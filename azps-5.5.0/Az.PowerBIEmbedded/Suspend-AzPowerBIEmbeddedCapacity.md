---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 18359b0086257719bc0d050629c532756634a89e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151178"
---
# <span data-ttu-id="efa53-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="efa53-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="efa53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa53-102">SYNOPSIS</span></span>
<span data-ttu-id="efa53-103">Felfüggeszti a PowerBI beágyazott kapacitásának egy példányát.</span><span class="sxs-lookup"><span data-stu-id="efa53-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="efa53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efa53-104">SYNTAX</span></span>

### <span data-ttu-id="efa53-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efa53-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa53-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="efa53-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa53-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="efa53-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa53-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efa53-108">DESCRIPTION</span></span>
<span data-ttu-id="efa53-109">A Suspend-AzPowerBIEmbeddedCapacity parancsmag felfüggeszti a PowerBI beágyazott kapacitásának egy példányát</span><span class="sxs-lookup"><span data-stu-id="efa53-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="efa53-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efa53-110">EXAMPLES</span></span>

### <span data-ttu-id="efa53-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="efa53-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="efa53-112">Ez a parancs felfüggeszti az erőforráscsoport tesztcsoportban a tesztkapacitás nevű aktív kapacitást.</span><span class="sxs-lookup"><span data-stu-id="efa53-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="efa53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efa53-113">PARAMETERS</span></span>

### <span data-ttu-id="efa53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa53-114">-DefaultProfile</span></span>
<span data-ttu-id="efa53-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efa53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa53-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa53-116">-InputObject</span></span>
<span data-ttu-id="efa53-117">Input object for Piping</span><span class="sxs-lookup"><span data-stu-id="efa53-117">Input object for Piping</span></span>

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

### <span data-ttu-id="efa53-118">-Name</span><span class="sxs-lookup"><span data-stu-id="efa53-118">-Name</span></span>
<span data-ttu-id="efa53-119">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="efa53-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="efa53-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efa53-120">-PassThru</span></span>
<span data-ttu-id="efa53-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="efa53-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="efa53-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa53-122">-ResourceGroupName</span></span>
<span data-ttu-id="efa53-123">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="efa53-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="efa53-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efa53-124">-ResourceId</span></span>
<span data-ttu-id="efa53-125">Azure-erőforrásazonosító</span><span class="sxs-lookup"><span data-stu-id="efa53-125">Azure resource ID</span></span>

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

### <span data-ttu-id="efa53-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efa53-126">-Confirm</span></span>
<span data-ttu-id="efa53-127">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="efa53-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="efa53-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa53-128">-WhatIf</span></span>
<span data-ttu-id="efa53-129">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="efa53-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="efa53-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa53-130">CommonParameters</span></span>
<span data-ttu-id="efa53-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa53-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa53-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa53-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa53-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efa53-133">INPUTS</span></span>

### <span data-ttu-id="efa53-134">System.String</span><span class="sxs-lookup"><span data-stu-id="efa53-134">System.String</span></span>

### <span data-ttu-id="efa53-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="efa53-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="efa53-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa53-136">OUTPUTS</span></span>

### <span data-ttu-id="efa53-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="efa53-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="efa53-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efa53-138">NOTES</span></span>

## <span data-ttu-id="efa53-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa53-139">RELATED LINKS</span></span>

[<span data-ttu-id="efa53-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="efa53-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="efa53-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="efa53-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

