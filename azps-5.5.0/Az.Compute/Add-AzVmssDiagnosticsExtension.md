---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204990"
---
# <span data-ttu-id="6e14e-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6e14e-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="6e14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e14e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e14e-103">Diagnosztikai bővítmény hozzáadása a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="6e14e-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="6e14e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e14e-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e14e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e14e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e14e-106">Az **Add-AzVmssDiagnosticsExtension** parancsmag hozzáad egy diagnosztikai bővítményt a VIRTUÁLISgép-mérethalmaz (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="6e14e-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6e14e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e14e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e14e-108">1. példa: Diagnosztikai bővítmény hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="6e14e-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="6e14e-109">Ez a parancs hozzáad egy diagnosztikai bővítményt a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="6e14e-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="6e14e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e14e-110">PARAMETERS</span></span>

### <span data-ttu-id="6e14e-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6e14e-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6e14e-112">Azt jelzi, hogy ez a parancsmag lehetővé teszi-e az Azure-vendégügynöknek, hogy automatikusan frissítse a bővítményt egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="6e14e-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e14e-113">-DefaultProfile</span></span>
<span data-ttu-id="6e14e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e14e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6e14e-115">-Force</span></span>
<span data-ttu-id="6e14e-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="6e14e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6e14e-117">-Name</span></span>
<span data-ttu-id="6e14e-118">Egy bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e14e-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="6e14e-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="6e14e-120">A privát konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e14e-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="6e14e-121">-SettingFilePath</span></span>
<span data-ttu-id="6e14e-122">A nyilvános konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e14e-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6e14e-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="6e14e-124">A VMSS-hez használt bővítmény verziója.</span><span class="sxs-lookup"><span data-stu-id="6e14e-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="6e14e-125">A verzió beszerzéséhez futtassa a [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmagot a *PublisherName* paraméterhez a Microsoft.Azure.Diagnostics értékkel, a *Type* paraméterhez pedig az IaaSDiagnostics parancsot.</span><span class="sxs-lookup"><span data-stu-id="6e14e-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6e14e-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6e14e-127">Adja meg a VMSS-objektumot.</span><span class="sxs-lookup"><span data-stu-id="6e14e-127">Specify the VMSS object.</span></span>
<span data-ttu-id="6e14e-128">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6e14e-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e14e-129">-Confirm</span></span>
<span data-ttu-id="6e14e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e14e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e14e-131">-WhatIf</span></span>
<span data-ttu-id="6e14e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e14e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e14e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e14e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e14e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e14e-134">CommonParameters</span></span>
<span data-ttu-id="6e14e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e14e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e14e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e14e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e14e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e14e-137">INPUTS</span></span>

### <span data-ttu-id="6e14e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6e14e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6e14e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6e14e-139">System.String</span></span>

### <span data-ttu-id="6e14e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e14e-140">System.Boolean</span></span>

## <span data-ttu-id="6e14e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e14e-141">OUTPUTS</span></span>

### <span data-ttu-id="6e14e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6e14e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6e14e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e14e-143">NOTES</span></span>

## <span data-ttu-id="6e14e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e14e-144">RELATED LINKS</span></span>

[<span data-ttu-id="6e14e-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6e14e-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="6e14e-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6e14e-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="6e14e-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6e14e-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
