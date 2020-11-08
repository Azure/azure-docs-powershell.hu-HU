---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182919"
---
# <span data-ttu-id="7df69-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7df69-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7df69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7df69-102">SYNOPSIS</span></span>
<span data-ttu-id="7df69-103">A PowerBI beágyazott kapacitás példányának törlése</span><span class="sxs-lookup"><span data-stu-id="7df69-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="7df69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7df69-104">SYNTAX</span></span>

### <span data-ttu-id="7df69-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7df69-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7df69-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7df69-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7df69-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7df69-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df69-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7df69-108">DESCRIPTION</span></span>
<span data-ttu-id="7df69-109">A Remove-AzPowerBIEmbeddedCapacity parancsmag törli a PowerBI beágyazott kapacitású példányát</span><span class="sxs-lookup"><span data-stu-id="7df69-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7df69-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7df69-110">EXAMPLES</span></span>

### <span data-ttu-id="7df69-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7df69-111">Example 1</span></span>
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

<span data-ttu-id="7df69-112">Ez a parancs eltávolítja a testcapacity nevű kapacitást a resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="7df69-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="7df69-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7df69-113">PARAMETERS</span></span>

### <span data-ttu-id="7df69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df69-114">-DefaultProfile</span></span>
<span data-ttu-id="7df69-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7df69-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df69-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7df69-116">-InputObject</span></span>
<span data-ttu-id="7df69-117">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="7df69-117">Input object for Piping</span></span>

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

### <span data-ttu-id="7df69-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7df69-118">-Name</span></span>
<span data-ttu-id="7df69-119">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="7df69-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="7df69-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7df69-120">-PassThru</span></span>
<span data-ttu-id="7df69-121">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="7df69-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="7df69-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df69-122">-ResourceGroupName</span></span>
<span data-ttu-id="7df69-123">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="7df69-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="7df69-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7df69-124">-ResourceId</span></span>
<span data-ttu-id="7df69-125">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="7df69-125">Azure resource ID</span></span>

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

### <span data-ttu-id="7df69-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7df69-126">-Confirm</span></span>
<span data-ttu-id="7df69-127">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="7df69-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7df69-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df69-128">-WhatIf</span></span>
<span data-ttu-id="7df69-129">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="7df69-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7df69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df69-130">CommonParameters</span></span>
<span data-ttu-id="7df69-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7df69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df69-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df69-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df69-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7df69-133">INPUTS</span></span>

### <span data-ttu-id="7df69-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7df69-134">System.String</span></span>

### <span data-ttu-id="7df69-135">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7df69-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7df69-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7df69-136">OUTPUTS</span></span>

### <span data-ttu-id="7df69-137">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7df69-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7df69-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7df69-138">NOTES</span></span>

## <span data-ttu-id="7df69-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7df69-139">RELATED LINKS</span></span>

[<span data-ttu-id="7df69-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7df69-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7df69-141">Új – AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7df69-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
