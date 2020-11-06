---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503459"
---
# <span data-ttu-id="c6521-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c6521-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c6521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6521-102">SYNOPSIS</span></span>
<span data-ttu-id="c6521-103">A PowerBI beágyazott kapacitás példányának módosítása.</span><span class="sxs-lookup"><span data-stu-id="c6521-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6521-104">SYNTAX</span></span>

### <span data-ttu-id="c6521-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6521-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6521-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6521-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6521-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6521-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6521-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6521-108">DESCRIPTION</span></span>
<span data-ttu-id="c6521-109">A Update-AzureRmPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitása egy példányát módosítja.</span><span class="sxs-lookup"><span data-stu-id="c6521-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="c6521-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c6521-110">EXAMPLES</span></span>

### <span data-ttu-id="c6521-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6521-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="c6521-112">Módosítja a testcapacity nevű resourcegroup-testgroup kapacitást a címkék beállításához key1: érték1 és azonosító2: érték2 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c6521-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="c6521-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6521-113">PARAMETERS</span></span>

### <span data-ttu-id="c6521-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="c6521-114">-Administrator</span></span>
<span data-ttu-id="c6521-115">Vesszővel elválasztott kapacitási nevek a kapacitás rendszergazdaként való beállításához</span><span class="sxs-lookup"><span data-stu-id="c6521-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="c6521-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6521-116">-DefaultProfile</span></span>
<span data-ttu-id="c6521-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6521-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6521-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6521-118">-InputObject</span></span>
<span data-ttu-id="c6521-119">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="c6521-119">Input object for Piping</span></span>

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

### <span data-ttu-id="c6521-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6521-120">-Name</span></span>
<span data-ttu-id="c6521-121">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="c6521-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="c6521-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6521-122">-PassThru</span></span>
<span data-ttu-id="c6521-123">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="c6521-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c6521-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6521-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6521-125">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="c6521-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="c6521-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6521-126">-ResourceId</span></span>
<span data-ttu-id="c6521-127">A PowerBI beágyazott kapacitás ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c6521-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="c6521-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6521-128">-Sku</span></span>
<span data-ttu-id="c6521-129">A kapacitáshoz tartozó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="c6521-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="c6521-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="c6521-130">-Tag</span></span>
<span data-ttu-id="c6521-131">A kulcs-érték párok egy kivonatoló táblázat formájában, amely a kapacitásban címkékként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="c6521-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="c6521-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6521-132">-Confirm</span></span>
<span data-ttu-id="c6521-133">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="c6521-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c6521-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6521-134">-WhatIf</span></span>
<span data-ttu-id="c6521-135">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="c6521-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c6521-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6521-136">CommonParameters</span></span>
<span data-ttu-id="c6521-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6521-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6521-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6521-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6521-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6521-139">INPUTS</span></span>

### <span data-ttu-id="c6521-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c6521-140">System.String</span></span>

### <span data-ttu-id="c6521-141">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c6521-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="c6521-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6521-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c6521-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6521-143">OUTPUTS</span></span>

### <span data-ttu-id="c6521-144">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c6521-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c6521-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6521-145">NOTES</span></span>

## <span data-ttu-id="c6521-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6521-146">RELATED LINKS</span></span>

[<span data-ttu-id="c6521-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c6521-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c6521-148">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c6521-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
