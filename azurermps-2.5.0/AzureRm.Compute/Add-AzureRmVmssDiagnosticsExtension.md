---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 8e6a0ec7002f211e660c3ca71d190faf719bbd6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848542"
---
# <span data-ttu-id="73cac-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73cac-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="73cac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73cac-102">SYNOPSIS</span></span>
<span data-ttu-id="73cac-103">Diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="73cac-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73cac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73cac-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73cac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73cac-105">DESCRIPTION</span></span>
<span data-ttu-id="73cac-106">Az **Add-AzureRmVmssDiagnosticsExtension** parancsmag a Virtual Machine Scale set (VMSS) példányhoz ad diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="73cac-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="73cac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73cac-107">EXAMPLES</span></span>

### <span data-ttu-id="73cac-108">Példa 1: diagnosztikai bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="73cac-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="73cac-109">Ez a parancs egy diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="73cac-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="73cac-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73cac-110">PARAMETERS</span></span>

### <span data-ttu-id="73cac-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="73cac-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="73cac-112">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="73cac-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cac-113">-DefaultProfile</span></span>
<span data-ttu-id="73cac-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73cac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-115">-Force</span><span class="sxs-lookup"><span data-stu-id="73cac-115">-Force</span></span>
<span data-ttu-id="73cac-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="73cac-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73cac-117">-Name</span></span>
<span data-ttu-id="73cac-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73cac-118">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="73cac-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="73cac-120">A privát konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="73cac-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="73cac-121">-SettingFilePath</span></span>
<span data-ttu-id="73cac-122">A nyilvános konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="73cac-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="73cac-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="73cac-124">Annak a bővítménynek a verzióját adja meg, amelyet a VMSS használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="73cac-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="73cac-125">A verzió beszerzéséhez futtassa a [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) parancsmagot a Microsoft. Azure. Diagnostics *PublisherName* paraméterének és IaaSDiagnostics a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="73cac-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73cac-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="73cac-127">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="73cac-127">Specify the VMSS object.</span></span>
<span data-ttu-id="73cac-128">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="73cac-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73cac-129">-Confirm</span></span>
<span data-ttu-id="73cac-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73cac-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cac-131">-WhatIf</span></span>
<span data-ttu-id="73cac-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73cac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73cac-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73cac-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cac-134">CommonParameters</span></span>
<span data-ttu-id="73cac-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73cac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cac-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73cac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cac-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73cac-137">INPUTS</span></span>

### <span data-ttu-id="73cac-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73cac-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="73cac-139">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="73cac-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="73cac-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73cac-140">OUTPUTS</span></span>

###  
<span data-ttu-id="73cac-141">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73cac-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="73cac-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73cac-142">NOTES</span></span>

## <span data-ttu-id="73cac-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73cac-143">RELATED LINKS</span></span>

[<span data-ttu-id="73cac-144">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="73cac-144">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="73cac-145">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73cac-145">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="73cac-146">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73cac-146">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
