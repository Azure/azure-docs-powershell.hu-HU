---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468762"
---
# <span data-ttu-id="fc306-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc306-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc306-102">SYNOPSIS</span></span>
<span data-ttu-id="fc306-103">Módosítja a PowerBI beágyazott kapacitásának egy példányát.</span><span class="sxs-lookup"><span data-stu-id="fc306-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fc306-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc306-104">SYNTAX</span></span>

### <span data-ttu-id="fc306-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc306-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc306-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc306-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc306-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc306-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc306-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc306-108">DESCRIPTION</span></span>
<span data-ttu-id="fc306-109">A Update-AzPowerBIEmbeddedCapacity parancsmag módosítja a PowerBI beágyazott kapacitásának egy példányát</span><span class="sxs-lookup"><span data-stu-id="fc306-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="fc306-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc306-110">EXAMPLES</span></span>

### <span data-ttu-id="fc306-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fc306-111">Example 1</span></span>
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

<span data-ttu-id="fc306-112">Módosítja a tesztkapacitás nevű kapacitást az erőforráscsoport tesztcsoportban, és a címkéket kulcs1:érték1 és key2:value2 és rendszergazdai jogosultságúként, valamint a testuser1@contoso.com testuser2@contoso.com szolgáltatásnévként adja meg: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="fc306-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="fc306-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc306-113">PARAMETERS</span></span>

### <span data-ttu-id="fc306-114">- Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="fc306-114">-Administrator</span></span>
<span data-ttu-id="fc306-115">Vesszővel elválasztott nevek, amelyek alapján a kapacitást rendszergazdákként állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="fc306-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="fc306-116">Egyszerű szolgáltatásnév: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="fc306-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="fc306-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc306-117">-DefaultProfile</span></span>
<span data-ttu-id="fc306-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc306-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc306-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc306-119">-InputObject</span></span>
<span data-ttu-id="fc306-120">Input object for Piping</span><span class="sxs-lookup"><span data-stu-id="fc306-120">Input object for Piping</span></span>

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

### <span data-ttu-id="fc306-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fc306-121">-Name</span></span>
<span data-ttu-id="fc306-122">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="fc306-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="fc306-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc306-123">-PassThru</span></span>
<span data-ttu-id="fc306-124">A törölt kapacitás adatait adja vissza, ha a művelet sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="fc306-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="fc306-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc306-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc306-126">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="fc306-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="fc306-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc306-127">-ResourceId</span></span>
<span data-ttu-id="fc306-128">PowerBI beágyazott kapacitási erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="fc306-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="fc306-129">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="fc306-129">-Sku</span></span>
<span data-ttu-id="fc306-130">A kapacitás termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="fc306-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="fc306-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc306-131">-Tag</span></span>
<span data-ttu-id="fc306-132">Kulcsérték-párok a kapacitás címkéiként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="fc306-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="fc306-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc306-133">-Confirm</span></span>
<span data-ttu-id="fc306-134">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="fc306-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="fc306-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc306-135">-WhatIf</span></span>
<span data-ttu-id="fc306-136">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="fc306-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="fc306-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc306-137">CommonParameters</span></span>
<span data-ttu-id="fc306-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc306-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc306-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc306-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc306-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc306-140">INPUTS</span></span>

### <span data-ttu-id="fc306-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fc306-141">System.String</span></span>

### <span data-ttu-id="fc306-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc306-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc306-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc306-143">OUTPUTS</span></span>

### <span data-ttu-id="fc306-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc306-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc306-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc306-145">NOTES</span></span>

## <span data-ttu-id="fc306-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc306-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc306-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc306-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="fc306-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc306-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
