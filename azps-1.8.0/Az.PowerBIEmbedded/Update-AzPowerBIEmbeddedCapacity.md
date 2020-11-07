---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669788"
---
# <span data-ttu-id="f021d-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f021d-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f021d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f021d-102">SYNOPSIS</span></span>
<span data-ttu-id="f021d-103">A PowerBI beágyazott kapacitás példányának módosítása.</span><span class="sxs-lookup"><span data-stu-id="f021d-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f021d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f021d-104">SYNTAX</span></span>

### <span data-ttu-id="f021d-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f021d-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f021d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f021d-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f021d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f021d-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f021d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f021d-108">DESCRIPTION</span></span>
<span data-ttu-id="f021d-109">A Update-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitása egy példányát módosítja.</span><span class="sxs-lookup"><span data-stu-id="f021d-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f021d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f021d-110">EXAMPLES</span></span>

### <span data-ttu-id="f021d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f021d-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="f021d-112">Módosítja a testcapacity nevű resourcegroup-testgroup kapacitást a címkék beállításához key1: érték1 és azonosító2: érték2 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f021d-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="f021d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f021d-113">PARAMETERS</span></span>

### <span data-ttu-id="f021d-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="f021d-114">-Administrator</span></span>
<span data-ttu-id="f021d-115">Vesszővel elválasztott kapacitási nevek a kapacitás rendszergazdaként való beállításához</span><span class="sxs-lookup"><span data-stu-id="f021d-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f021d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f021d-116">-DefaultProfile</span></span>
<span data-ttu-id="f021d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f021d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f021d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f021d-118">-InputObject</span></span>
<span data-ttu-id="f021d-119">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="f021d-119">Input object for Piping</span></span>

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

### <span data-ttu-id="f021d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f021d-120">-Name</span></span>
<span data-ttu-id="f021d-121">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="f021d-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="f021d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f021d-122">-PassThru</span></span>
<span data-ttu-id="f021d-123">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="f021d-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f021d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f021d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f021d-125">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="f021d-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="f021d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f021d-126">-ResourceId</span></span>
<span data-ttu-id="f021d-127">A PowerBI beágyazott kapacitás ResourceID.</span><span class="sxs-lookup"><span data-stu-id="f021d-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="f021d-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="f021d-128">-Sku</span></span>
<span data-ttu-id="f021d-129">A kapacitáshoz tartozó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="f021d-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f021d-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="f021d-130">-Tag</span></span>
<span data-ttu-id="f021d-131">A kulcs-érték párok egy kivonatoló táblázat formájában, amely a kapacitásban címkékként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="f021d-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f021d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f021d-132">-Confirm</span></span>
<span data-ttu-id="f021d-133">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="f021d-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f021d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f021d-134">-WhatIf</span></span>
<span data-ttu-id="f021d-135">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="f021d-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f021d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f021d-136">CommonParameters</span></span>
<span data-ttu-id="f021d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f021d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f021d-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f021d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f021d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f021d-139">INPUTS</span></span>

### <span data-ttu-id="f021d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f021d-140">System.String</span></span>

### <span data-ttu-id="f021d-141">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f021d-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f021d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f021d-142">OUTPUTS</span></span>

### <span data-ttu-id="f021d-143">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f021d-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f021d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f021d-144">NOTES</span></span>

## <span data-ttu-id="f021d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f021d-145">RELATED LINKS</span></span>

[<span data-ttu-id="f021d-146">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f021d-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f021d-147">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f021d-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
