---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186861"
---
# <span data-ttu-id="8a904-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8a904-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8a904-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a904-102">SYNOPSIS</span></span>
<span data-ttu-id="8a904-103">Folytatja a PowerBI beágyazott kapacitások példányát.</span><span class="sxs-lookup"><span data-stu-id="8a904-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="8a904-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a904-104">SYNTAX</span></span>

### <span data-ttu-id="8a904-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a904-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a904-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a904-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a904-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a904-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a904-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a904-108">DESCRIPTION</span></span>
<span data-ttu-id="8a904-109">Az Resume-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásának egy példányát folytatja.</span><span class="sxs-lookup"><span data-stu-id="8a904-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="8a904-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8a904-110">EXAMPLES</span></span>

### <span data-ttu-id="8a904-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8a904-111">Example 1</span></span>
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

<span data-ttu-id="8a904-112">Ez a parancs folytatja a testcapacity nevű felfüggesztett kapacitást a resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="8a904-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="8a904-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a904-113">PARAMETERS</span></span>

### <span data-ttu-id="8a904-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a904-114">-DefaultProfile</span></span>
<span data-ttu-id="8a904-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a904-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a904-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a904-116">-InputObject</span></span>
<span data-ttu-id="8a904-117">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="8a904-117">Input object for Piping</span></span>

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

### <span data-ttu-id="8a904-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a904-118">-Name</span></span>
<span data-ttu-id="8a904-119">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="8a904-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="8a904-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a904-120">-PassThru</span></span>
<span data-ttu-id="8a904-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8a904-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8a904-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a904-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a904-123">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="8a904-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="8a904-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a904-124">-ResourceId</span></span>
<span data-ttu-id="8a904-125">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="8a904-125">Azure resource ID</span></span>

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

### <span data-ttu-id="8a904-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a904-126">-Confirm</span></span>
<span data-ttu-id="8a904-127">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="8a904-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="8a904-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a904-128">-WhatIf</span></span>
<span data-ttu-id="8a904-129">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="8a904-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="8a904-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a904-130">CommonParameters</span></span>
<span data-ttu-id="8a904-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a904-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a904-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a904-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a904-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a904-133">INPUTS</span></span>

### <span data-ttu-id="8a904-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8a904-134">System.String</span></span>

### <span data-ttu-id="8a904-135">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8a904-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8a904-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a904-136">OUTPUTS</span></span>

### <span data-ttu-id="8a904-137">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8a904-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8a904-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a904-138">NOTES</span></span>

## <span data-ttu-id="8a904-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a904-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a904-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8a904-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8a904-141">Felfüggesztés – AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8a904-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
