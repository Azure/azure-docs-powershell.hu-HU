---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298784"
---
# <span data-ttu-id="c5738-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="c5738-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="c5738-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5738-102">SYNOPSIS</span></span>
<span data-ttu-id="c5738-103">Új megrendelést hoz létre egy eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="c5738-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="c5738-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5738-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5738-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5738-105">DESCRIPTION</span></span>
<span data-ttu-id="c5738-106">A **New-AzDataBoxEdgeOrder** parancsmag új sorrendet hoz létre az adatmező Edge-eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="c5738-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="c5738-107">A rendelés létrehozása előtt először létre kell hozva egy adatmező-Edge-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c5738-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="c5738-108">Megadhatja, hogy miként hozhatja létre a sorrendet a partnerek, a cégnév, az e-mailek, a cím stb.</span><span class="sxs-lookup"><span data-stu-id="c5738-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="c5738-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c5738-109">EXAMPLES</span></span>

### <span data-ttu-id="c5738-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c5738-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="c5738-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5738-111">PARAMETERS</span></span>

### <span data-ttu-id="c5738-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="c5738-112">-AddressLine1</span></span>
<span data-ttu-id="c5738-113">A cím első sora</span><span class="sxs-lookup"><span data-stu-id="c5738-113">Address first line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="c5738-114">-AddressLine2</span></span>
<span data-ttu-id="c5738-115">Cím második sora</span><span class="sxs-lookup"><span data-stu-id="c5738-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="c5738-116">-AddressLine3</span></span>
<span data-ttu-id="c5738-117">Cím harmadik sora</span><span class="sxs-lookup"><span data-stu-id="c5738-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5738-118">-AsJob</span></span>
<span data-ttu-id="c5738-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c5738-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5738-120">-Város</span><span class="sxs-lookup"><span data-stu-id="c5738-120">-City</span></span>
<span data-ttu-id="c5738-121">A város neve</span><span class="sxs-lookup"><span data-stu-id="c5738-121">Name of the City</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-122">-Vállalatnév</span><span class="sxs-lookup"><span data-stu-id="c5738-122">-CompanyName</span></span>
<span data-ttu-id="c5738-123">A cég neve</span><span class="sxs-lookup"><span data-stu-id="c5738-123">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="c5738-124">-ContactPerson</span></span>
<span data-ttu-id="c5738-125">A kapcsolattartó neve</span><span class="sxs-lookup"><span data-stu-id="c5738-125">Name of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-126">-Ország</span><span class="sxs-lookup"><span data-stu-id="c5738-126">-Country</span></span>
<span data-ttu-id="c5738-127">Az ország neve</span><span class="sxs-lookup"><span data-stu-id="c5738-127">Name of the Country</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5738-128">-DefaultProfile</span></span>
<span data-ttu-id="c5738-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5738-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5738-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c5738-130">-DeviceName</span></span>
<span data-ttu-id="c5738-131">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="c5738-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-132">– E-mail</span><span class="sxs-lookup"><span data-stu-id="c5738-132">-Email</span></span>
<span data-ttu-id="c5738-133">A frissítések fogadására szolgáló e-mailek listája, elfogadja a 10 e-mailek maximumát.</span><span class="sxs-lookup"><span data-stu-id="c5738-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="c5738-134">-Phone</span></span>
<span data-ttu-id="c5738-135">A Kapcsolattartó telefonszáma</span><span class="sxs-lookup"><span data-stu-id="c5738-135">Phone number of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-136">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="c5738-136">-PostalCode</span></span>
<span data-ttu-id="c5738-137">A cím postai kódja</span><span class="sxs-lookup"><span data-stu-id="c5738-137">Postal Code of the Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5738-138">-ResourceGroupName</span></span>
<span data-ttu-id="c5738-139">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c5738-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-140">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c5738-140">-State</span></span>
<span data-ttu-id="c5738-141">Az állam neve</span><span class="sxs-lookup"><span data-stu-id="c5738-141">Name of the State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5738-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5738-142">-Confirm</span></span>
<span data-ttu-id="c5738-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5738-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5738-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5738-144">-WhatIf</span></span>
<span data-ttu-id="c5738-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5738-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5738-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5738-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5738-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5738-147">CommonParameters</span></span>
<span data-ttu-id="c5738-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5738-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5738-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c5738-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5738-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5738-150">INPUTS</span></span>

### <span data-ttu-id="c5738-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c5738-151">System.String</span></span>

## <span data-ttu-id="c5738-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5738-152">OUTPUTS</span></span>

### <span data-ttu-id="c5738-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="c5738-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="c5738-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5738-154">NOTES</span></span>

## <span data-ttu-id="c5738-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5738-155">RELATED LINKS</span></span>
