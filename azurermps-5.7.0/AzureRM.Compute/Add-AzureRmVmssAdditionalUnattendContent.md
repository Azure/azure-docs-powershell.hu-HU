---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494561"
---
# <span data-ttu-id="4695a-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="4695a-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="4695a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4695a-102">SYNOPSIS</span></span>
<span data-ttu-id="4695a-103">Információt ad a Windows felügyelet nélküli telepítési fájljához.</span><span class="sxs-lookup"><span data-stu-id="4695a-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4695a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4695a-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4695a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4695a-105">DESCRIPTION</span></span>
<span data-ttu-id="4695a-106">Az **Add-AzureRmVmssAdditionalUnattendContent** parancsmag információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="4695a-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4695a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4695a-107">EXAMPLES</span></span>

### <span data-ttu-id="4695a-108">1. példa: adatok hozzáadása a Windows felügyelet nélküli telepítésének megválaszolása</span><span class="sxs-lookup"><span data-stu-id="4695a-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="4695a-109">Ez a parancs információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="4695a-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4695a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4695a-110">PARAMETERS</span></span>

### <span data-ttu-id="4695a-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="4695a-111">-ComponentName</span></span>
<span data-ttu-id="4695a-112">A hozzáadott tartalommal konfigurált összetevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4695a-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="4695a-113">Az egyetlen megengedhető érték a Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="4695a-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4695a-114">-Content (tartalom)</span><span class="sxs-lookup"><span data-stu-id="4695a-114">-Content</span></span>
<span data-ttu-id="4695a-115">A megadott elérési útra és összetevőre vonatkozó unattend.xml-fájlhoz hozzáadott XML formátumú tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4695a-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4695a-116">-PassName</span><span class="sxs-lookup"><span data-stu-id="4695a-116">-PassName</span></span>
<span data-ttu-id="4695a-117">Megadja annak a továbbításnak a nevét, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4695a-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="4695a-118">Az egyetlen megengedhető érték az oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="4695a-118">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4695a-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="4695a-119">-SettingName</span></span>
<span data-ttu-id="4695a-120">Annak a beállításnak a neve, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4695a-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="4695a-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4695a-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="4695a-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="4695a-122">FirstLogonCommands</span></span>
- <span data-ttu-id="4695a-123">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="4695a-123">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4695a-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4695a-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4695a-125">Adja meg a virtuálisgép- **készlet** objektumát.</span><span class="sxs-lookup"><span data-stu-id="4695a-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="4695a-126">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4695a-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4695a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4695a-127">-Confirm</span></span>
<span data-ttu-id="4695a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4695a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4695a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4695a-129">-WhatIf</span></span>
<span data-ttu-id="4695a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4695a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4695a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4695a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4695a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4695a-132">CommonParameters</span></span>
<span data-ttu-id="4695a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4695a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4695a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4695a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4695a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4695a-135">INPUTS</span></span>

### <span data-ttu-id="4695a-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="4695a-136">None</span></span>
<span data-ttu-id="4695a-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4695a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4695a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4695a-138">OUTPUTS</span></span>

## <span data-ttu-id="4695a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4695a-139">NOTES</span></span>

## <span data-ttu-id="4695a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4695a-140">RELATED LINKS</span></span>

[<span data-ttu-id="4695a-141">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4695a-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
