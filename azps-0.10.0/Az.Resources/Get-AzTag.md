---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 1f2289351da276a0422828c082bb51d8dc267a20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843389"
---
# <span data-ttu-id="a8240-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="a8240-101">Get-AzTag</span></span>

## <span data-ttu-id="a8240-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8240-102">SYNOPSIS</span></span>
<span data-ttu-id="a8240-103">Előre definiált Azure-címkéket kap.</span><span class="sxs-lookup"><span data-stu-id="a8240-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="a8240-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8240-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8240-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8240-105">DESCRIPTION</span></span>
<span data-ttu-id="a8240-106">A **Get-AzTag** parancsmag előre meghatározott Azure-címkéket kap az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a8240-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="a8240-107">Ez a parancsmag alapvető információkat ad a címkékről vagy a címkékről és az azok értékeiről.</span><span class="sxs-lookup"><span data-stu-id="a8240-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="a8240-108">Minden kimeneti objektum tartalmazza a Count tulajdonságot, amely az erőforrások és az erőforráscsoportok számát adja meg, és a címkéket és az értékeket alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="a8240-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="a8240-109">A **Get-AzTag** Azure címkéi modul segítséget nyújt az előre definiált Azure-címkék kezelésében.</span><span class="sxs-lookup"><span data-stu-id="a8240-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="a8240-110">Az Azure címke olyan név-érték páros, amellyel az Azure-erőforrásokat és az erőforráscsoportokat (például részleg vagy költséghely) kategorizálhatja, illetve az erőforrásokkal és csoportokkal kapcsolatos megjegyzéseket és megjegyzéseket követheti.</span><span class="sxs-lookup"><span data-stu-id="a8240-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="a8240-111">A címkéket egyetlen lépésben definiálhatja és alkalmazhatja, de az előre definiált címkék segítségével megadhatja az előfizetésben szereplő címkék standard, egységes, kiszámítható nevét és értékét.</span><span class="sxs-lookup"><span data-stu-id="a8240-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="a8240-112">Ha előre definiált címkét szeretne létrehozni, használja az New-AzTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a8240-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="a8240-113">Ha egy erőforráscsoport számára előre meghatározott címkét szeretne alkalmazni, használja az New-AzTag parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="a8240-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="a8240-114">Ha egy adott címke vagy név és érték esetén szeretne erőforrás-csoportokat keresni, használja az Get-AzResourceGroup parancsmag *címke* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="a8240-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="a8240-115">Példák</span><span class="sxs-lookup"><span data-stu-id="a8240-115">EXAMPLES</span></span>

### <span data-ttu-id="a8240-116">Példa 1: az összes előre definiált címke beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8240-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="a8240-117">Ez a parancs az előfizetésben minden előre definiált címkét kap.</span><span class="sxs-lookup"><span data-stu-id="a8240-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="a8240-118">A Count tulajdonság azt jeleníti meg, hogy hányszor alkalmazta a címkét az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="a8240-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="a8240-119">2. példa: név szerinti címke beszerzése</span><span class="sxs-lookup"><span data-stu-id="a8240-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="a8240-120">Ez a parancs részletes információkat kap a részleg címkéről és annak értékeiről.</span><span class="sxs-lookup"><span data-stu-id="a8240-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="a8240-121">A Count tulajdonság azt jeleníti meg, hogy hányszor lett alkalmazva a címke és az egyes értékek az előfizetésben szereplő erőforrásokra és erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="a8240-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="a8240-122">3. példa: az összes címke értékének beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8240-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="a8240-123">Ez a parancs a *részletes* adatokat részletesen részletezi az előfizetésben szereplő összes előre definiált címkével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="a8240-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="a8240-124">A *részletes* paraméter a minden címkéhez tartozó *Name* paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="a8240-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="a8240-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8240-125">PARAMETERS</span></span>

### <span data-ttu-id="a8240-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8240-126">-DefaultProfile</span></span>
<span data-ttu-id="a8240-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8240-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8240-128">– Részletes</span><span class="sxs-lookup"><span data-stu-id="a8240-128">-Detailed</span></span>
<span data-ttu-id="a8240-129">Azt jelzi, hogy ez a művelet a kimenetre vonatkozó értékek címkézésével kapcsolatos információkat ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="a8240-129">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8240-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8240-130">-Name</span></span>
<span data-ttu-id="a8240-131">A beolvasott címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8240-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="a8240-132">Alapértelmezés szerint a **Get-AzTag** az előfizetésben szereplő összes előre definiált címkére vonatkozó alapvető információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8240-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="a8240-133">A *Name* paraméter megadásakor a *részletes* paraméternek nincs eredménye.</span><span class="sxs-lookup"><span data-stu-id="a8240-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8240-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8240-134">CommonParameters</span></span>
<span data-ttu-id="a8240-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8240-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8240-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8240-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8240-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8240-137">INPUTS</span></span>

### <span data-ttu-id="a8240-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8240-138">System.String</span></span>

### <span data-ttu-id="a8240-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8240-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8240-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8240-140">OUTPUTS</span></span>

### <span data-ttu-id="a8240-141">Microsoft. Azure. Command. ResourceManager. comm. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="a8240-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="a8240-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8240-142">NOTES</span></span>

## <span data-ttu-id="a8240-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8240-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8240-144">Új – AzTag</span><span class="sxs-lookup"><span data-stu-id="a8240-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="a8240-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="a8240-145">Remove-AzTag</span></span>](./Remove-AzTag.md)

