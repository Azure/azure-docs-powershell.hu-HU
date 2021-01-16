---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362094"
---
# <span data-ttu-id="ad453-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="ad453-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="ad453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad453-102">SYNOPSIS</span></span>
<span data-ttu-id="ad453-103">Létrehoz egy támogatási kapcsolattartó-profilobjektumot.</span><span class="sxs-lookup"><span data-stu-id="ad453-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="ad453-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad453-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad453-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad453-105">DESCRIPTION</span></span>
<span data-ttu-id="ad453-106">Ez egy súgó parancsmag, amely egy támogatási jegy létrehozásakor vagy frissítésekénél használható támogatási kapcsolatprofil-objektum létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="ad453-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="ad453-107">Meg kell adnia az alábbi paramétereket, amelyek kötelezőek a támogatási jegy létrehozásához:</span><span class="sxs-lookup"><span data-stu-id="ad453-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="ad453-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad453-108">EXAMPLES</span></span>

### <span data-ttu-id="ad453-109">1. példa: Névjegyobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ad453-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="ad453-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad453-110">PARAMETERS</span></span>

### <span data-ttu-id="ad453-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ad453-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="ad453-112">Az itt felsorolt e-mail-címeket a rendszer a támogatási jegyről küldött minden levélre átmásolja.</span><span class="sxs-lookup"><span data-stu-id="ad453-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="ad453-113">-Country</span><span class="sxs-lookup"><span data-stu-id="ad453-113">-Country</span></span>
<span data-ttu-id="ad453-114">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="ad453-114">Customer country.</span></span>
<span data-ttu-id="ad453-115">Érvényes ISO Alfa-3 országkódnak (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ad453-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="ad453-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad453-116">-DefaultProfile</span></span>
<span data-ttu-id="ad453-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad453-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad453-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ad453-118">-FirstName</span></span>
<span data-ttu-id="ad453-119">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="ad453-119">Customer first name.</span></span>

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

### <span data-ttu-id="ad453-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="ad453-120">-LastName</span></span>
<span data-ttu-id="ad453-121">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="ad453-121">Customer last name.</span></span>

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

### <span data-ttu-id="ad453-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="ad453-122">-PhoneNumber</span></span>
<span data-ttu-id="ad453-123">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="ad453-123">Customer phone number.</span></span>
<span data-ttu-id="ad453-124">Erre akkor van szükség, ha az előnyben részesített kapcsolatfelvételi mód a telefon.</span><span class="sxs-lookup"><span data-stu-id="ad453-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="ad453-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="ad453-125">-PreferredContactMethod</span></span>
<span data-ttu-id="ad453-126">Előnyben részesített kapcsolatfelvételi mód.</span><span class="sxs-lookup"><span data-stu-id="ad453-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad453-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="ad453-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="ad453-128">Az ügyfél elsődleges támogatási nyelve.</span><span class="sxs-lookup"><span data-stu-id="ad453-128">Customer preferred support language.</span></span>
<span data-ttu-id="ad453-129">A kódnak érvényesnek kell lennie az itt felsorolt nyelvek https://azure.microsoft.com/support/faq/ egyikében.</span><span class="sxs-lookup"><span data-stu-id="ad453-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="ad453-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="ad453-130">-PreferredTimeZone</span></span>
<span data-ttu-id="ad453-131">Ügyfél által előnyben részesített időzóna.</span><span class="sxs-lookup"><span data-stu-id="ad453-131">Customer preferred time zone.</span></span>
<span data-ttu-id="ad453-132">Ennek érvényes System.TimeZoneInfo.Id kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ad453-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="ad453-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ad453-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="ad453-134">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="ad453-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="ad453-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad453-135">-Confirm</span></span>
<span data-ttu-id="ad453-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad453-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad453-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad453-137">-WhatIf</span></span>
<span data-ttu-id="ad453-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad453-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad453-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad453-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad453-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad453-140">CommonParameters</span></span>
<span data-ttu-id="ad453-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad453-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad453-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad453-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad453-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad453-143">INPUTS</span></span>

### <span data-ttu-id="ad453-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="ad453-144">None</span></span>

## <span data-ttu-id="ad453-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad453-145">OUTPUTS</span></span>

### <span data-ttu-id="ad453-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="ad453-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="ad453-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad453-147">NOTES</span></span>

## <span data-ttu-id="ad453-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad453-148">RELATED LINKS</span></span>
