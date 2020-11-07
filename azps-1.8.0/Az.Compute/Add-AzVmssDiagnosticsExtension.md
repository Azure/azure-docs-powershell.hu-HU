---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 32f3cfa8f9e27a9b54e0b103ec09195946ac3e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671375"
---
# <span data-ttu-id="491cb-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="491cb-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="491cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="491cb-102">SYNOPSIS</span></span>
<span data-ttu-id="491cb-103">Diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="491cb-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="491cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="491cb-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="491cb-105">DESCRIPTION</span></span>
<span data-ttu-id="491cb-106">Az **Add-AzVmssDiagnosticsExtension** parancsmag a Virtual Machine Scale set (VMSS) példányhoz ad diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="491cb-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="491cb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="491cb-107">EXAMPLES</span></span>

### <span data-ttu-id="491cb-108">Példa 1: diagnosztikai bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="491cb-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="491cb-109">Ez a parancs egy diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="491cb-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="491cb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="491cb-110">PARAMETERS</span></span>

### <span data-ttu-id="491cb-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="491cb-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="491cb-112">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="491cb-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="491cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491cb-113">-DefaultProfile</span></span>
<span data-ttu-id="491cb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="491cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="491cb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="491cb-115">-Force</span></span>
<span data-ttu-id="491cb-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="491cb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="491cb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="491cb-117">-Name</span></span>
<span data-ttu-id="491cb-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="491cb-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="491cb-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="491cb-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="491cb-120">A privát konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="491cb-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="491cb-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="491cb-121">-SettingFilePath</span></span>
<span data-ttu-id="491cb-122">A nyilvános konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="491cb-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="491cb-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="491cb-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="491cb-124">Annak a bővítménynek a verzióját adja meg, amelyet a VMSS használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="491cb-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="491cb-125">A verzió beszerzéséhez futtassa a [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmagot a Microsoft. Azure. Diagnostics *PublisherName* paraméterének és IaaSDiagnostics a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="491cb-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="491cb-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="491cb-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="491cb-127">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="491cb-127">Specify the VMSS object.</span></span>
<span data-ttu-id="491cb-128">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="491cb-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="491cb-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="491cb-129">-Confirm</span></span>
<span data-ttu-id="491cb-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="491cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="491cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491cb-131">-WhatIf</span></span>
<span data-ttu-id="491cb-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="491cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="491cb-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="491cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="491cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491cb-134">CommonParameters</span></span>
<span data-ttu-id="491cb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="491cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491cb-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491cb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491cb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="491cb-137">INPUTS</span></span>

### <span data-ttu-id="491cb-138">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="491cb-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="491cb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="491cb-139">System.String</span></span>

### <span data-ttu-id="491cb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="491cb-140">System.Boolean</span></span>

## <span data-ttu-id="491cb-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="491cb-141">OUTPUTS</span></span>

### <span data-ttu-id="491cb-142">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="491cb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="491cb-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="491cb-143">NOTES</span></span>

## <span data-ttu-id="491cb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="491cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="491cb-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="491cb-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="491cb-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="491cb-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="491cb-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="491cb-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
