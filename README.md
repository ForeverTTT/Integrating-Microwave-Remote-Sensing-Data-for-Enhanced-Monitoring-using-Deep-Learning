## Integrating Microwave Remote Sensing Data for Enhanced Monitoring

Lightweight overview of the repository layout and key entry points.

### Structure
- `Diffusion/`
  - `config/diffusion.yaml`: default configuration for training/inference.
  - `data/lrhr_dataset.py`: dataset loader for low-/high-resolution pairs.
  - `models/diffusion_model.py`: core diffusion network definition.
  - `training/diffusion_trainer.py`: training loop and checkpoints.
  - `scripts/diffusion_infer.py`: inference script using trained weights.
  - `utils/encoding.py`: helper utilities (e.g., positional encodings).
  - `requirements.txt`: Python dependencies for diffusion workflow.
- `Vit/`
  - `vit.py`: vision transformer model.
  - `train.py` / `train_VV_VH.py`: training entry points for different channel setups.
  - `infer.py` / `infer_VV_VH.py`: inference scripts matching the training variants.
  - `lrhr_dataset.py` / `lrhr_dataset_VV_VH.py`: dataset loaders for single- or dual-polarization inputs.
  - `transfer.py`: transfer learning or fine-tuning utility.
  - `README.md`: additional notes specific to the ViT pipeline.
- `Final Report.pdf`: project report.

### Getting Started
1. Create a virtual environment and install dependencies per `Diffusion/requirements.txt` (and any noted in `Vit/README.md`).
2. Prepare datasets expected by the loaders in `Diffusion/data/` or `Vit/`.
3. Run training via the corresponding `train*.py` (ViT) or `Diffusion/training/diffusion_trainer.py`.
4. Perform inference with `scripts/diffusion_infer.py` (diffusion) or the `infer*.py` scripts (ViT), pointing to trained checkpoints.

