---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339078"
---
# <span data-ttu-id="46ddc-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="46ddc-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="46ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="46ddc-103">Új rendelést hoz létre egy eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="46ddc-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="46ddc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46ddc-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ddc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="46ddc-106">A **New-AzDataBoxEdgeOrder** parancsmag új sorrendet hoz létre egy Data Box Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="46ddc-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="46ddc-107">A rendelés létrehozása előtt először létre kell hozzon egy Data Box Edge-eszközerőforrást.</span><span class="sxs-lookup"><span data-stu-id="46ddc-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="46ddc-108">A rendelés létrehozásához megadhatja az olyan adatokat, mint a kapcsolattartó, a cég neve, az e-mail-cím stb. a sorrend létrehozásához szükséges paraméterek.</span><span class="sxs-lookup"><span data-stu-id="46ddc-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="46ddc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46ddc-109">EXAMPLES</span></span>

### <span data-ttu-id="46ddc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="46ddc-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="46ddc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46ddc-111">PARAMETERS</span></span>

### <span data-ttu-id="46ddc-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="46ddc-112">-AddressLine1</span></span>
<span data-ttu-id="46ddc-113">Cím első sor</span><span class="sxs-lookup"><span data-stu-id="46ddc-113">Address first line</span></span>

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

### <span data-ttu-id="46ddc-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="46ddc-114">-AddressLine2</span></span>
<span data-ttu-id="46ddc-115">Cím második sor</span><span class="sxs-lookup"><span data-stu-id="46ddc-115">Address second line</span></span>

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

### <span data-ttu-id="46ddc-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="46ddc-116">-AddressLine3</span></span>
<span data-ttu-id="46ddc-117">Cím – harmadik sor</span><span class="sxs-lookup"><span data-stu-id="46ddc-117">Address third line</span></span>

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

### <span data-ttu-id="46ddc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46ddc-118">-AsJob</span></span>
<span data-ttu-id="46ddc-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="46ddc-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46ddc-120">-City</span><span class="sxs-lookup"><span data-stu-id="46ddc-120">-City</span></span>
<span data-ttu-id="46ddc-121">A város neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-121">Name of the City</span></span>

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

### <span data-ttu-id="46ddc-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="46ddc-122">-CompanyName</span></span>
<span data-ttu-id="46ddc-123">A vállalat neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-123">Name of the company</span></span>

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

### <span data-ttu-id="46ddc-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="46ddc-124">-ContactPerson</span></span>
<span data-ttu-id="46ddc-125">A partner neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-125">Name of the contact person</span></span>

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

### <span data-ttu-id="46ddc-126">-Country</span><span class="sxs-lookup"><span data-stu-id="46ddc-126">-Country</span></span>
<span data-ttu-id="46ddc-127">Az ország neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-127">Name of the Country</span></span>

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

### <span data-ttu-id="46ddc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ddc-128">-DefaultProfile</span></span>
<span data-ttu-id="46ddc-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46ddc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ddc-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="46ddc-130">-DeviceName</span></span>
<span data-ttu-id="46ddc-131">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-131">Resource Name</span></span>

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

### <span data-ttu-id="46ddc-132">-Email</span><span class="sxs-lookup"><span data-stu-id="46ddc-132">-Email</span></span>
<span data-ttu-id="46ddc-133">A frissítéseket megkapó e-mailek listája, Legfeljebb 10 e-mail elfogadása</span><span class="sxs-lookup"><span data-stu-id="46ddc-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="46ddc-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="46ddc-134">-Phone</span></span>
<span data-ttu-id="46ddc-135">A partner telefonszáma</span><span class="sxs-lookup"><span data-stu-id="46ddc-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="46ddc-136">-Irányítószám</span><span class="sxs-lookup"><span data-stu-id="46ddc-136">-PostalCode</span></span>
<span data-ttu-id="46ddc-137">A cím irányítószáma</span><span class="sxs-lookup"><span data-stu-id="46ddc-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="46ddc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ddc-138">-ResourceGroupName</span></span>
<span data-ttu-id="46ddc-139">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-139">Resource Group Name</span></span>

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

### <span data-ttu-id="46ddc-140">-State</span><span class="sxs-lookup"><span data-stu-id="46ddc-140">-State</span></span>
<span data-ttu-id="46ddc-141">Az állam neve</span><span class="sxs-lookup"><span data-stu-id="46ddc-141">Name of the State</span></span>

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

### <span data-ttu-id="46ddc-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46ddc-142">-Confirm</span></span>
<span data-ttu-id="46ddc-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="46ddc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ddc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ddc-144">-WhatIf</span></span>
<span data-ttu-id="46ddc-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="46ddc-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46ddc-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46ddc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ddc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ddc-147">CommonParameters</span></span>
<span data-ttu-id="46ddc-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ddc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ddc-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46ddc-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ddc-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46ddc-150">INPUTS</span></span>

### <span data-ttu-id="46ddc-151">System.String</span><span class="sxs-lookup"><span data-stu-id="46ddc-151">System.String</span></span>

## <span data-ttu-id="46ddc-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46ddc-152">OUTPUTS</span></span>

### <span data-ttu-id="46ddc-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="46ddc-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="46ddc-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46ddc-154">NOTES</span></span>

## <span data-ttu-id="46ddc-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46ddc-155">RELATED LINKS</span></span>
