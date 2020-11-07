---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8a406ebfe6c919dad30e7a394b0b4a4c912cf557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838710"
---
# <span data-ttu-id="eb08d-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb08d-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eb08d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb08d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb08d-103">Felfüggeszti a PowerBI beágyazott kapacitás példányát.</span><span class="sxs-lookup"><span data-stu-id="eb08d-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="eb08d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb08d-104">SYNTAX</span></span>

### <span data-ttu-id="eb08d-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb08d-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb08d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb08d-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb08d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb08d-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb08d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb08d-108">DESCRIPTION</span></span>
<span data-ttu-id="eb08d-109">Az Suspend-AzPowerBIEmbeddedCapacity parancsmag felfüggeszti a PowerBI beágyazott kapacitásának példányát</span><span class="sxs-lookup"><span data-stu-id="eb08d-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="eb08d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eb08d-110">EXAMPLES</span></span>

### <span data-ttu-id="eb08d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb08d-111">Example 1</span></span>
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

<span data-ttu-id="eb08d-112">Ez a parancs felfüggeszti a testcapacity nevű aktív kapacitást a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="eb08d-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="eb08d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb08d-113">PARAMETERS</span></span>

### <span data-ttu-id="eb08d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb08d-114">-DefaultProfile</span></span>
<span data-ttu-id="eb08d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb08d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb08d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb08d-116">-InputObject</span></span>
<span data-ttu-id="eb08d-117">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="eb08d-117">Input object for Piping</span></span>

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

### <span data-ttu-id="eb08d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb08d-118">-Name</span></span>
<span data-ttu-id="eb08d-119">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="eb08d-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="eb08d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb08d-120">-PassThru</span></span>
<span data-ttu-id="eb08d-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eb08d-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eb08d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb08d-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb08d-123">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="eb08d-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="eb08d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb08d-124">-ResourceId</span></span>
<span data-ttu-id="eb08d-125">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="eb08d-125">Azure resource ID</span></span>

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

### <span data-ttu-id="eb08d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb08d-126">-Confirm</span></span>
<span data-ttu-id="eb08d-127">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="eb08d-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="eb08d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb08d-128">-WhatIf</span></span>
<span data-ttu-id="eb08d-129">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="eb08d-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="eb08d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb08d-130">CommonParameters</span></span>
<span data-ttu-id="eb08d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb08d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb08d-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb08d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb08d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb08d-133">INPUTS</span></span>

### <span data-ttu-id="eb08d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eb08d-134">System.String</span></span>

### <span data-ttu-id="eb08d-135">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb08d-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eb08d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb08d-136">OUTPUTS</span></span>

### <span data-ttu-id="eb08d-137">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb08d-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eb08d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb08d-138">NOTES</span></span>

## <span data-ttu-id="eb08d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb08d-139">RELATED LINKS</span></span>

[<span data-ttu-id="eb08d-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb08d-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="eb08d-141">Önéletrajz – AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb08d-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

