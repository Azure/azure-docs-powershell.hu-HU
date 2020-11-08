---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183682"
---
# <span data-ttu-id="2e04a-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2e04a-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="2e04a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e04a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e04a-103">Diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e04a-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="2e04a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e04a-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e04a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e04a-105">DESCRIPTION</span></span>
<span data-ttu-id="2e04a-106">Az **Add-AzVmssDiagnosticsExtension** parancsmag a Virtual Machine Scale set (VMSS) példányhoz ad diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2e04a-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2e04a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e04a-107">EXAMPLES</span></span>

### <span data-ttu-id="2e04a-108">Példa 1: diagnosztikai bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="2e04a-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="2e04a-109">Ez a parancs egy diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="2e04a-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="2e04a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e04a-110">PARAMETERS</span></span>

### <span data-ttu-id="2e04a-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2e04a-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2e04a-112">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="2e04a-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="2e04a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e04a-113">-DefaultProfile</span></span>
<span data-ttu-id="2e04a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e04a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e04a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2e04a-115">-Force</span></span>
<span data-ttu-id="2e04a-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2e04a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e04a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e04a-117">-Name</span></span>
<span data-ttu-id="2e04a-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e04a-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="2e04a-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="2e04a-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="2e04a-120">A privát konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e04a-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="2e04a-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="2e04a-121">-SettingFilePath</span></span>
<span data-ttu-id="2e04a-122">A nyilvános konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e04a-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="2e04a-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2e04a-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="2e04a-124">Annak a bővítménynek a verzióját adja meg, amelyet a VMSS használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="2e04a-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="2e04a-125">A verzió beszerzéséhez futtassa a [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmagot a Microsoft. Azure. Diagnostics *PublisherName* paraméterének és IaaSDiagnostics a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="2e04a-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="2e04a-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e04a-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2e04a-127">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="2e04a-127">Specify the VMSS object.</span></span>
<span data-ttu-id="2e04a-128">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2e04a-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="2e04a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e04a-129">-Confirm</span></span>
<span data-ttu-id="2e04a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e04a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e04a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e04a-131">-WhatIf</span></span>
<span data-ttu-id="2e04a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e04a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e04a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e04a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e04a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e04a-134">CommonParameters</span></span>
<span data-ttu-id="2e04a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e04a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e04a-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e04a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e04a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e04a-137">INPUTS</span></span>

### <span data-ttu-id="2e04a-138">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e04a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2e04a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2e04a-139">System.String</span></span>

### <span data-ttu-id="2e04a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e04a-140">System.Boolean</span></span>

## <span data-ttu-id="2e04a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e04a-141">OUTPUTS</span></span>

### <span data-ttu-id="2e04a-142">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e04a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2e04a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e04a-143">NOTES</span></span>

## <span data-ttu-id="2e04a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e04a-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e04a-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2e04a-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="2e04a-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2e04a-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="2e04a-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2e04a-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
