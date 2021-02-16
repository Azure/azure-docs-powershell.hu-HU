---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145011"
---
# <span data-ttu-id="aefbc-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="aefbc-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="aefbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefbc-102">SYNOPSIS</span></span>
<span data-ttu-id="aefbc-103">Információkat ad a felügyelet nélküli Windows Setup válaszfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="aefbc-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="aefbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aefbc-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aefbc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aefbc-105">DESCRIPTION</span></span>
<span data-ttu-id="aefbc-106">Az **Add-AzVmssAdditionalUnattendContent** parancsmag információkat ad a felügyelet nélküli Windows Setup válaszfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="aefbc-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="aefbc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aefbc-107">EXAMPLES</span></span>

### <span data-ttu-id="aefbc-108">1. példa: Adatok hozzáadása a felügyelet nélküli Windows Setup válaszfájlhoz</span><span class="sxs-lookup"><span data-stu-id="aefbc-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="aefbc-109">Ez a parancs információkat ad a felügyelet nélküli Windows Setup válaszfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="aefbc-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="aefbc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aefbc-110">PARAMETERS</span></span>

### <span data-ttu-id="aefbc-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="aefbc-111">-ComponentName</span></span>
<span data-ttu-id="aefbc-112">Annak az összetevőnek a nevét adja meg, amely a hozzáadott tartalommal együtt konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="aefbc-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="aefbc-113">Az egyetlen megengedett érték a Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="aefbc-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="aefbc-114">-Content</span><span class="sxs-lookup"><span data-stu-id="aefbc-114">-Content</span></span>
<span data-ttu-id="aefbc-115">A megadott elérési úthoz és összetevőhez unattend.xml XML formátumú tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="aefbc-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="aefbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefbc-116">-DefaultProfile</span></span>
<span data-ttu-id="aefbc-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aefbc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aefbc-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="aefbc-118">-PassName</span></span>
<span data-ttu-id="aefbc-119">Annak a passznak a neve, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="aefbc-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="aefbc-120">Az egyetlen megengedett érték az oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="aefbc-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="aefbc-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="aefbc-121">-SettingName</span></span>
<span data-ttu-id="aefbc-122">Annak a beállításnak a nevét adja meg, amelyre a tartalom vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="aefbc-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="aefbc-123">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="aefbc-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="aefbc-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="aefbc-124">FirstLogonCommands</span></span>
- <span data-ttu-id="aefbc-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="aefbc-125">AutoLogon</span></span>

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

### <span data-ttu-id="aefbc-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aefbc-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="aefbc-127">Adja meg a virtuális gép **Scale Set objektumát.**</span><span class="sxs-lookup"><span data-stu-id="aefbc-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="aefbc-128">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aefbc-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="aefbc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aefbc-129">-Confirm</span></span>
<span data-ttu-id="aefbc-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aefbc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefbc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefbc-131">-WhatIf</span></span>
<span data-ttu-id="aefbc-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aefbc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aefbc-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aefbc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefbc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefbc-134">CommonParameters</span></span>
<span data-ttu-id="aefbc-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aefbc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefbc-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aefbc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefbc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aefbc-137">INPUTS</span></span>

### <span data-ttu-id="aefbc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aefbc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="aefbc-139">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aefbc-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="aefbc-140">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aefbc-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="aefbc-141">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aefbc-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="aefbc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="aefbc-142">System.String</span></span>

## <span data-ttu-id="aefbc-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aefbc-143">OUTPUTS</span></span>

### <span data-ttu-id="aefbc-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aefbc-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="aefbc-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aefbc-145">NOTES</span></span>

## <span data-ttu-id="aefbc-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aefbc-146">RELATED LINKS</span></span>

[<span data-ttu-id="aefbc-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="aefbc-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
