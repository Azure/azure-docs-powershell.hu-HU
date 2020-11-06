---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4370a7b87ee87b223ddadd6f872b549c2537e1e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498340"
---
# <span data-ttu-id="a0266-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a0266-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="a0266-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0266-102">SYNOPSIS</span></span>
<span data-ttu-id="a0266-103">Diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0266-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0266-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0266-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0266-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0266-105">DESCRIPTION</span></span>
<span data-ttu-id="a0266-106">Az **Add-AzureRmVmssDiagnosticsExtension** parancsmag a Virtual Machine Scale set (VMSS) példányhoz ad diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a0266-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a0266-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0266-107">EXAMPLES</span></span>

### <span data-ttu-id="a0266-108">Példa 1: diagnosztikai bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="a0266-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="a0266-109">Ez a parancs egy diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0266-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="a0266-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0266-110">PARAMETERS</span></span>

### <span data-ttu-id="a0266-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a0266-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a0266-112">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a0266-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="a0266-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0266-113">-DefaultProfile</span></span>
<span data-ttu-id="a0266-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0266-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0266-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0266-115">-Force</span></span>
<span data-ttu-id="a0266-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a0266-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0266-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0266-117">-Name</span></span>
<span data-ttu-id="a0266-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0266-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="a0266-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="a0266-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="a0266-120">A privát konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0266-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="a0266-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="a0266-121">-SettingFilePath</span></span>
<span data-ttu-id="a0266-122">A nyilvános konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0266-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="a0266-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a0266-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="a0266-124">Annak a bővítménynek a verzióját adja meg, amelyet a VMSS használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="a0266-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="a0266-125">A verzió beszerzéséhez futtassa a [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) parancsmagot a Microsoft. Azure. Diagnostics *PublisherName* paraméterének és IaaSDiagnostics a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="a0266-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="a0266-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0266-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a0266-127">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="a0266-127">Specify the VMSS object.</span></span>
<span data-ttu-id="a0266-128">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a0266-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a0266-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0266-129">-Confirm</span></span>
<span data-ttu-id="a0266-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0266-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0266-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0266-131">-WhatIf</span></span>
<span data-ttu-id="a0266-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0266-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0266-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0266-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0266-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0266-134">CommonParameters</span></span>
<span data-ttu-id="a0266-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0266-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0266-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0266-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0266-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0266-137">INPUTS</span></span>

### <span data-ttu-id="a0266-138">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0266-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

### <span data-ttu-id="a0266-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a0266-139">System.String</span></span>

### <span data-ttu-id="a0266-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0266-140">System.Boolean</span></span>

## <span data-ttu-id="a0266-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0266-141">OUTPUTS</span></span>

### <span data-ttu-id="a0266-142">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0266-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="a0266-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0266-143">NOTES</span></span>

## <span data-ttu-id="a0266-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0266-144">RELATED LINKS</span></span>

[<span data-ttu-id="a0266-145">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a0266-145">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="a0266-146">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a0266-146">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="a0266-147">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a0266-147">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
