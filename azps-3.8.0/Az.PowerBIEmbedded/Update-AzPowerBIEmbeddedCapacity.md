---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014469"
---
# <span data-ttu-id="2f516-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2f516-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2f516-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f516-102">SYNOPSIS</span></span>
<span data-ttu-id="2f516-103">A PowerBI beágyazott kapacitás példányának módosítása.</span><span class="sxs-lookup"><span data-stu-id="2f516-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="2f516-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f516-104">SYNTAX</span></span>

### <span data-ttu-id="2f516-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f516-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f516-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f516-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f516-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f516-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f516-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f516-108">DESCRIPTION</span></span>
<span data-ttu-id="2f516-109">A Update-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitása egy példányát módosítja.</span><span class="sxs-lookup"><span data-stu-id="2f516-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2f516-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f516-110">EXAMPLES</span></span>

### <span data-ttu-id="2f516-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f516-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="2f516-112">Módosítja a testcapacity nevű resourcegroup testgroup-as kapacitást a címkék key1: érték1 és azonosító2: érték2, a rendszergazda testuser1@contoso.com testuser2@contoso.com és a megbízó között: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="2f516-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="2f516-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f516-113">PARAMETERS</span></span>

### <span data-ttu-id="2f516-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="2f516-114">-Administrator</span></span>
<span data-ttu-id="2f516-115">Vesszővel elválasztott nevek, amelyeket rendszergazdaként kell beállítani a kapacitásban.</span><span class="sxs-lookup"><span data-stu-id="2f516-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="2f516-116">Egyszerű szolgáltatásnév esetén: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="2f516-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="2f516-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f516-117">-DefaultProfile</span></span>
<span data-ttu-id="2f516-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f516-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f516-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f516-119">-InputObject</span></span>
<span data-ttu-id="2f516-120">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="2f516-120">Input object for Piping</span></span>

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

### <span data-ttu-id="2f516-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f516-121">-Name</span></span>
<span data-ttu-id="2f516-122">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="2f516-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="2f516-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f516-123">-PassThru</span></span>
<span data-ttu-id="2f516-124">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="2f516-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2f516-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f516-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f516-126">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="2f516-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="2f516-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f516-127">-ResourceId</span></span>
<span data-ttu-id="2f516-128">A PowerBI beágyazott kapacitás ResourceID.</span><span class="sxs-lookup"><span data-stu-id="2f516-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="2f516-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="2f516-129">-Sku</span></span>
<span data-ttu-id="2f516-130">A kapacitáshoz tartozó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="2f516-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="2f516-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="2f516-131">-Tag</span></span>
<span data-ttu-id="2f516-132">A kulcs-érték párok egy kivonatoló táblázat formájában, amely a kapacitásban címkékként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="2f516-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="2f516-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f516-133">-Confirm</span></span>
<span data-ttu-id="2f516-134">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="2f516-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2f516-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f516-135">-WhatIf</span></span>
<span data-ttu-id="2f516-136">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="2f516-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2f516-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f516-137">CommonParameters</span></span>
<span data-ttu-id="2f516-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f516-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f516-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f516-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f516-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f516-140">INPUTS</span></span>

### <span data-ttu-id="2f516-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2f516-141">System.String</span></span>

### <span data-ttu-id="2f516-142">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2f516-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2f516-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f516-143">OUTPUTS</span></span>

### <span data-ttu-id="2f516-144">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2f516-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2f516-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f516-145">NOTES</span></span>

## <span data-ttu-id="2f516-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f516-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f516-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2f516-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2f516-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2f516-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
