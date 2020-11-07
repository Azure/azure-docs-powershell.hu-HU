---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: f84d9f823d97872d8ad2491a2ab45ef3bb5a22a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844714"
---
# <span data-ttu-id="8bb66-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8bb66-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="8bb66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bb66-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb66-103">Diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="8bb66-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="8bb66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bb66-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bb66-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bb66-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb66-106">Az **Add-AzVmssDiagnosticsExtension** parancsmag a Virtual Machine Scale set (VMSS) példányhoz ad diagnosztikai bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8bb66-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8bb66-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8bb66-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb66-108">Példa 1: diagnosztikai bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="8bb66-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="8bb66-109">Ez a parancs egy diagnosztikai bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="8bb66-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="8bb66-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bb66-110">PARAMETERS</span></span>

### <span data-ttu-id="8bb66-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8bb66-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8bb66-112">Azt jelzi, hogy a parancsmag lehetővé teszi-e az Azure Guest Agent számára, hogy egy újabb alverzióra automatikusan frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8bb66-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="8bb66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb66-113">-DefaultProfile</span></span>
<span data-ttu-id="8bb66-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bb66-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb66-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8bb66-115">-Force</span></span>
<span data-ttu-id="8bb66-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8bb66-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8bb66-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8bb66-117">-Name</span></span>
<span data-ttu-id="8bb66-118">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bb66-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="8bb66-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="8bb66-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="8bb66-120">A privát konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bb66-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="8bb66-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="8bb66-121">-SettingFilePath</span></span>
<span data-ttu-id="8bb66-122">A nyilvános konfigurációs fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bb66-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="8bb66-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8bb66-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="8bb66-124">Annak a bővítménynek a verzióját adja meg, amelyet a VMSS használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="8bb66-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="8bb66-125">A verzió beszerzéséhez futtassa a [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmagot a Microsoft. Azure. Diagnostics *PublisherName* paraméterének és IaaSDiagnostics a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="8bb66-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="8bb66-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8bb66-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8bb66-127">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="8bb66-127">Specify the VMSS object.</span></span>
<span data-ttu-id="8bb66-128">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8bb66-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="8bb66-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bb66-129">-Confirm</span></span>
<span data-ttu-id="8bb66-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bb66-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb66-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb66-131">-WhatIf</span></span>
<span data-ttu-id="8bb66-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8bb66-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb66-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bb66-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb66-134">CommonParameters</span></span>
<span data-ttu-id="8bb66-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bb66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb66-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb66-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb66-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bb66-137">INPUTS</span></span>

### <span data-ttu-id="8bb66-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8bb66-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="8bb66-139">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8bb66-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="8bb66-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bb66-140">OUTPUTS</span></span>

###  
<span data-ttu-id="8bb66-141">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8bb66-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8bb66-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bb66-142">NOTES</span></span>

## <span data-ttu-id="8bb66-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bb66-143">RELATED LINKS</span></span>

[<span data-ttu-id="8bb66-144">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8bb66-144">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="8bb66-145">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8bb66-145">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="8bb66-146">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8bb66-146">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
