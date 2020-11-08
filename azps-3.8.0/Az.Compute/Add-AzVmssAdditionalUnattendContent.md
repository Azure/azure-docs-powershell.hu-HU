---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013442"
---
# <span data-ttu-id="4455a-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="4455a-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="4455a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4455a-102">SYNOPSIS</span></span>
<span data-ttu-id="4455a-103">Információt ad a Windows felügyelet nélküli telepítési fájljához.</span><span class="sxs-lookup"><span data-stu-id="4455a-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4455a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4455a-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4455a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4455a-105">DESCRIPTION</span></span>
<span data-ttu-id="4455a-106">Az **Add-AzVmssAdditionalUnattendContent** parancsmag információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="4455a-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4455a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4455a-107">EXAMPLES</span></span>

### <span data-ttu-id="4455a-108">1. példa: adatok hozzáadása a Windows felügyelet nélküli telepítésének megválaszolása</span><span class="sxs-lookup"><span data-stu-id="4455a-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="4455a-109">Ez a parancs információt ad a Windows felügyelet nélküli telepítéséről.</span><span class="sxs-lookup"><span data-stu-id="4455a-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="4455a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4455a-110">PARAMETERS</span></span>

### <span data-ttu-id="4455a-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="4455a-111">-ComponentName</span></span>
<span data-ttu-id="4455a-112">A hozzáadott tartalommal konfigurált összetevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4455a-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="4455a-113">Az egyetlen megengedhető érték a Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="4455a-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4455a-114">-Content (tartalom)</span><span class="sxs-lookup"><span data-stu-id="4455a-114">-Content</span></span>
<span data-ttu-id="4455a-115">A megadott elérési útra és összetevőre vonatkozó unattend.xml-fájlhoz hozzáadott XML formátumú tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4455a-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4455a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4455a-116">-DefaultProfile</span></span>
<span data-ttu-id="4455a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4455a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4455a-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="4455a-118">-PassName</span></span>
<span data-ttu-id="4455a-119">Megadja annak a továbbításnak a nevét, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4455a-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="4455a-120">Az egyetlen megengedhető érték az oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="4455a-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4455a-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="4455a-121">-SettingName</span></span>
<span data-ttu-id="4455a-122">Annak a beállításnak a neve, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4455a-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="4455a-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4455a-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="4455a-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="4455a-124">FirstLogonCommands</span></span>
- <span data-ttu-id="4455a-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="4455a-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4455a-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4455a-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4455a-127">Adja meg a virtuálisgép- **készlet** objektumát.</span><span class="sxs-lookup"><span data-stu-id="4455a-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="4455a-128">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4455a-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4455a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4455a-129">-Confirm</span></span>
<span data-ttu-id="4455a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4455a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4455a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4455a-131">-WhatIf</span></span>
<span data-ttu-id="4455a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4455a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4455a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4455a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4455a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4455a-134">CommonParameters</span></span>
<span data-ttu-id="4455a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4455a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4455a-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4455a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4455a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4455a-137">INPUTS</span></span>

### <span data-ttu-id="4455a-138">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4455a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4455a-139">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. PassNames, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4455a-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4455a-140">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ComponentNames, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4455a-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4455a-141">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. SettingNames, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4455a-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4455a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4455a-142">System.String</span></span>

## <span data-ttu-id="4455a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4455a-143">OUTPUTS</span></span>

### <span data-ttu-id="4455a-144">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4455a-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4455a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4455a-145">NOTES</span></span>

## <span data-ttu-id="4455a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4455a-146">RELATED LINKS</span></span>

[<span data-ttu-id="4455a-147">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4455a-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
