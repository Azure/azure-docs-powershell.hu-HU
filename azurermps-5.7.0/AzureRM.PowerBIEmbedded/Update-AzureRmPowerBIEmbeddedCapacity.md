---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492239"
---
# <span data-ttu-id="d7b5c-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d7b5c-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d7b5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b5c-103">A PowerBI beágyazott kapacitás példányának módosítása.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7b5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7b5c-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="d7b5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b5c-106">A Update-AzureRmPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitása egy példányát módosítja.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d7b5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7b5c-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b5c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7b5c-108">Example 1</span></span>
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

<span data-ttu-id="d7b5c-109">Módosítja a testcapacity nevű resourcegroup-testgroup kapacitást a címkék beállításához key1: érték1 és azonosító2: érték2 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d7b5c-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="d7b5c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7b5c-110">PARAMETERS</span></span>

### <span data-ttu-id="d7b5c-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7b5c-111">-Name</span></span>
<span data-ttu-id="d7b5c-112">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="d7b5c-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b5c-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7b5c-114">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="d7b5c-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="d7b5c-115">-Sku</span></span>
<span data-ttu-id="d7b5c-116">A kapacitáshoz tartozó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-117">-Címke</span><span class="sxs-lookup"><span data-stu-id="d7b5c-117">-Tag</span></span>
<span data-ttu-id="d7b5c-118">A kulcs-érték párok egy kivonatoló táblázat formájában, amely a kapacitásban címkékként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="d7b5c-119">-Administrator</span><span class="sxs-lookup"><span data-stu-id="d7b5c-119">-Administrator</span></span>
<span data-ttu-id="d7b5c-120">Vesszővel elválasztott kapacitási nevek a kapacitás rendszergazdaként való beállításához</span><span class="sxs-lookup"><span data-stu-id="d7b5c-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7b5c-121">-ResourceId</span></span>
<span data-ttu-id="d7b5c-122">A PowerBI beágyazott kapacitás ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7b5c-123">-InputObject</span></span>
<span data-ttu-id="d7b5c-124">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="d7b5c-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7b5c-125">-PassThru</span></span>
<span data-ttu-id="d7b5c-126">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="d7b5c-126">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7b5c-127">-Confirm</span></span>
<span data-ttu-id="d7b5c-128">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="d7b5c-128">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b5c-129">-WhatIf</span></span>
<span data-ttu-id="d7b5c-130">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="d7b5c-130">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b5c-131">CommonParameters</span></span>
<span data-ttu-id="d7b5c-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7b5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b5c-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b5c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b5c-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b5c-134">INPUTS</span></span>

### <span data-ttu-id="d7b5c-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7b5c-135">None</span></span>
<span data-ttu-id="d7b5c-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7b5c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b5c-137">OUTPUTS</span></span>

### <span data-ttu-id="d7b5c-138">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d7b5c-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d7b5c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7b5c-139">NOTES</span></span>

## <span data-ttu-id="d7b5c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7b5c-140">RELATED LINKS</span></span>

[<span data-ttu-id="d7b5c-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d7b5c-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d7b5c-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d7b5c-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
