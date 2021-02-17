
# Helper scripts

Maintenance scripts used in other packages.

## generate-vectors-from-arm-startup.sh

Script to generate the vectors_xxx.c files for a family.

Provide the path to the CMSIS assembly files, like
`${HOME}/STM32Cube/Repository/STM32Cube_FW_F0_V1.11.1/Drivers/CMSIS/Device/ST/STM32F0xx/Source/Templates/arm`
and the path to the destination folder, like
`eclipse-embed-cdt.github/eclipse-plugins.git/plugins/org.eclipse.embedcdt.templates.stm/templates/micro-os-plus/stm32f0.pack/src/cmsis`:

```bash
bash generate-vectors-from-arm-startup.sh ${from} ${to}
```

## convert-arm-asm-to-c.sh

Script to convert the Arm assembly file into C.

The input file is usually from the vendor CMSIS, something like `${HOME}/STM32Cube/Repository/STM32Cube_FW_F0_V1.11.1/Drivers/CMSIS/Device/ST/STM32F0xx/Source/Templates/arm/startup_stm32f030x6.s`

```bash
bash convert-arm-asm-to-c.sh ${input} >${output}
```

## clone-and-link-all-git-repos.sh

Script to download all source xPacks.

The first argument is an optional destination folder path.
