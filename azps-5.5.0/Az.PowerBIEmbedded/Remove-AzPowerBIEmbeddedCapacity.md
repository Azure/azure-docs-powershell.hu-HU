---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151187"
---
# <span data-ttu-id="c006b-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c006b-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c006b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c006b-102">SYNOPSIS</span></span>
<span data-ttu-id="c006b-103">Törli a PowerBI beágyazott kapacitásának egy példányát.</span><span class="sxs-lookup"><span data-stu-id="c006b-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="c006b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c006b-104">SYNTAX</span></span>

### <span data-ttu-id="c006b-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c006b-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c006b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c006b-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c006b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c006b-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c006b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c006b-108">DESCRIPTION</span></span>
<span data-ttu-id="c006b-109">A Remove-AzPowerBIEmbeddedCapacity parancsmag törli a PowerBI beágyazott kapacitásának egy példányát</span><span class="sxs-lookup"><span data-stu-id="c006b-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="c006b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c006b-110">EXAMPLES</span></span>

### <span data-ttu-id="c006b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c006b-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="c006b-112">Ez a parancs eltávolítja a tesztképesség-kapacitást az erőforráscsoport tesztRG-ében</span><span class="sxs-lookup"><span data-stu-id="c006b-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="c006b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c006b-113">PARAMETERS</span></span>

### <span data-ttu-id="c006b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c006b-114">-DefaultProfile</span></span>
<span data-ttu-id="c006b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c006b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c006b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c006b-116">-InputObject</span></span>
<span data-ttu-id="c006b-117">Input object for Piping</span><span class="sxs-lookup"><span data-stu-id="c006b-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c006b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c006b-118">-Name</span></span>
<span data-ttu-id="c006b-119">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="c006b-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c006b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c006b-120">-PassThru</span></span>
<span data-ttu-id="c006b-121">A törölt kapacitás adatait adja vissza, ha a művelet sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="c006b-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c006b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c006b-122">-ResourceGroupName</span></span>
<span data-ttu-id="c006b-123">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="c006b-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c006b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c006b-124">-ResourceId</span></span>
<span data-ttu-id="c006b-125">Azure-erőforrásazonosító</span><span class="sxs-lookup"><span data-stu-id="c006b-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c006b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c006b-126">-Confirm</span></span>
<span data-ttu-id="c006b-127">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="c006b-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c006b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c006b-128">-WhatIf</span></span>
<span data-ttu-id="c006b-129">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="c006b-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c006b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c006b-130">CommonParameters</span></span>
<span data-ttu-id="c006b-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c006b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c006b-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c006b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c006b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c006b-133">INPUTS</span></span>

### <span data-ttu-id="c006b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c006b-134">System.String</span></span>

### <span data-ttu-id="c006b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c006b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c006b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c006b-136">OUTPUTS</span></span>

### <span data-ttu-id="c006b-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c006b-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c006b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c006b-138">NOTES</span></span>

## <span data-ttu-id="c006b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c006b-139">RELATED LINKS</span></span>

[<span data-ttu-id="c006b-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c006b-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c006b-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c006b-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
