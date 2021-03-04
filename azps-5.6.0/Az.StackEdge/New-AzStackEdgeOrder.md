---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: 4cb6c46f3cadae9d36ec273fe7d6198e35927c81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933609"
---
# <span data-ttu-id="d3a4b-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d3a4b-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="d3a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a4b-103">Új rendelést hoz létre egy eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="d3a4b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3a4b-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a4b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a4b-106">A **New-AzStackEdgeOrder** parancsmag új sorrendet hoz létre a Stack Edge-es eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="d3a4b-107">A rendelés létrehozása előtt először létre kell hozzon egy Stack Edge típusú eszközerőforrást.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="d3a4b-108">A rendelés létrehozásához megadhatja az olyan adatokat, mint a kapcsolattartó, a cég neve, az e-mail-cím stb. a sorrend létrehozásához szükséges paraméterek.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="d3a4b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3a4b-109">EXAMPLES</span></span>

### <span data-ttu-id="d3a4b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d3a4b-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="d3a4b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a4b-111">PARAMETERS</span></span>

### <span data-ttu-id="d3a4b-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="d3a4b-112">-AddressLine1</span></span>
<span data-ttu-id="d3a4b-113">Cím első sor</span><span class="sxs-lookup"><span data-stu-id="d3a4b-113">Address first line</span></span>

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

### <span data-ttu-id="d3a4b-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="d3a4b-114">-AddressLine2</span></span>
<span data-ttu-id="d3a4b-115">Cím második sor</span><span class="sxs-lookup"><span data-stu-id="d3a4b-115">Address second line</span></span>

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

### <span data-ttu-id="d3a4b-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="d3a4b-116">-AddressLine3</span></span>
<span data-ttu-id="d3a4b-117">Cím – harmadik sor</span><span class="sxs-lookup"><span data-stu-id="d3a4b-117">Address third line</span></span>

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

### <span data-ttu-id="d3a4b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3a4b-118">-AsJob</span></span>
<span data-ttu-id="d3a4b-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d3a4b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3a4b-120">-City</span><span class="sxs-lookup"><span data-stu-id="d3a4b-120">-City</span></span>
<span data-ttu-id="d3a4b-121">A város neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-121">Name of the City</span></span>

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

### <span data-ttu-id="d3a4b-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="d3a4b-122">-CompanyName</span></span>
<span data-ttu-id="d3a4b-123">A vállalat neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-123">Name of the company</span></span>

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

### <span data-ttu-id="d3a4b-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="d3a4b-124">-ContactPerson</span></span>
<span data-ttu-id="d3a4b-125">A partner neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-125">Name of the contact person</span></span>

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

### <span data-ttu-id="d3a4b-126">-Country</span><span class="sxs-lookup"><span data-stu-id="d3a4b-126">-Country</span></span>
<span data-ttu-id="d3a4b-127">Az ország neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-127">Name of the Country</span></span>

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

### <span data-ttu-id="d3a4b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a4b-128">-DefaultProfile</span></span>
<span data-ttu-id="d3a4b-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a4b-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d3a4b-130">-DeviceName</span></span>
<span data-ttu-id="d3a4b-131">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-131">Resource Name</span></span>

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

### <span data-ttu-id="d3a4b-132">-Email</span><span class="sxs-lookup"><span data-stu-id="d3a4b-132">-Email</span></span>
<span data-ttu-id="d3a4b-133">A frissítéseket megkapó e-mailek listája, Legfeljebb 10 e-mail elfogadása</span><span class="sxs-lookup"><span data-stu-id="d3a4b-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="d3a4b-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="d3a4b-134">-Phone</span></span>
<span data-ttu-id="d3a4b-135">A partner telefonszáma</span><span class="sxs-lookup"><span data-stu-id="d3a4b-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="d3a4b-136">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="d3a4b-136">-PostalCode</span></span>
<span data-ttu-id="d3a4b-137">A cím irányítószáma</span><span class="sxs-lookup"><span data-stu-id="d3a4b-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="d3a4b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a4b-138">-ResourceGroupName</span></span>
<span data-ttu-id="d3a4b-139">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-139">Resource Group Name</span></span>

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

### <span data-ttu-id="d3a4b-140">-State</span><span class="sxs-lookup"><span data-stu-id="d3a4b-140">-State</span></span>
<span data-ttu-id="d3a4b-141">Az állam neve</span><span class="sxs-lookup"><span data-stu-id="d3a4b-141">Name of the State</span></span>

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

### <span data-ttu-id="d3a4b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3a4b-142">-Confirm</span></span>
<span data-ttu-id="d3a4b-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a4b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a4b-144">-WhatIf</span></span>
<span data-ttu-id="d3a4b-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3a4b-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a4b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a4b-147">CommonParameters</span></span>
<span data-ttu-id="d3a4b-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a4b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a4b-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a4b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a4b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a4b-150">INPUTS</span></span>

### <span data-ttu-id="d3a4b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a4b-151">System.String</span></span>

## <span data-ttu-id="d3a4b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3a4b-152">OUTPUTS</span></span>

### <span data-ttu-id="d3a4b-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d3a4b-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="d3a4b-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3a4b-154">NOTES</span></span>

## <span data-ttu-id="d3a4b-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3a4b-155">RELATED LINKS</span></span>
