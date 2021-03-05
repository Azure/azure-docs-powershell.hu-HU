---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: cd0eab8d5670f8c37d45c8e0e211100749aa7a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016165"
---
# <span data-ttu-id="33189-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33189-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="33189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33189-102">SYNOPSIS</span></span>
<span data-ttu-id="33189-103">A PowerBI beágyazott kapacitásának egy példányának folytatása.</span><span class="sxs-lookup"><span data-stu-id="33189-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="33189-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33189-104">SYNTAX</span></span>

### <span data-ttu-id="33189-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33189-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33189-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33189-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33189-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33189-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33189-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33189-108">DESCRIPTION</span></span>
<span data-ttu-id="33189-109">A Resume-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásának egy példányát folytatja</span><span class="sxs-lookup"><span data-stu-id="33189-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="33189-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33189-110">EXAMPLES</span></span>

### <span data-ttu-id="33189-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="33189-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="33189-112">Ez a parancs egy tesztkapacitás nevű szüneteltetett kapacitást fog folytatni az erőforráscsoport tesztRG-ében</span><span class="sxs-lookup"><span data-stu-id="33189-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="33189-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33189-113">PARAMETERS</span></span>

### <span data-ttu-id="33189-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33189-114">-DefaultProfile</span></span>
<span data-ttu-id="33189-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33189-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33189-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33189-116">-InputObject</span></span>
<span data-ttu-id="33189-117">Input object for Piping</span><span class="sxs-lookup"><span data-stu-id="33189-117">Input object for Piping</span></span>

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

### <span data-ttu-id="33189-118">-Name</span><span class="sxs-lookup"><span data-stu-id="33189-118">-Name</span></span>
<span data-ttu-id="33189-119">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="33189-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="33189-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33189-120">-PassThru</span></span>
<span data-ttu-id="33189-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="33189-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="33189-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33189-122">-ResourceGroupName</span></span>
<span data-ttu-id="33189-123">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="33189-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="33189-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33189-124">-ResourceId</span></span>
<span data-ttu-id="33189-125">Azure-erőforrásazonosító</span><span class="sxs-lookup"><span data-stu-id="33189-125">Azure resource ID</span></span>

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

### <span data-ttu-id="33189-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33189-126">-Confirm</span></span>
<span data-ttu-id="33189-127">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="33189-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="33189-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33189-128">-WhatIf</span></span>
<span data-ttu-id="33189-129">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="33189-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="33189-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33189-130">CommonParameters</span></span>
<span data-ttu-id="33189-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33189-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33189-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33189-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33189-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33189-133">INPUTS</span></span>

### <span data-ttu-id="33189-134">System.String</span><span class="sxs-lookup"><span data-stu-id="33189-134">System.String</span></span>

### <span data-ttu-id="33189-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33189-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="33189-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33189-136">OUTPUTS</span></span>

### <span data-ttu-id="33189-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33189-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="33189-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33189-138">NOTES</span></span>

## <span data-ttu-id="33189-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33189-139">RELATED LINKS</span></span>

[<span data-ttu-id="33189-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33189-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="33189-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33189-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
