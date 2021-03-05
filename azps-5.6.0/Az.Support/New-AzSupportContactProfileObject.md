---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 5b2dfbc472b128a12f108aafc92aa9d30b661255
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002165"
---
# <span data-ttu-id="05ff0-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="05ff0-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="05ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="05ff0-103">Létrehoz egy támogatási kapcsolattartó-profilobjektumot.</span><span class="sxs-lookup"><span data-stu-id="05ff0-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="05ff0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05ff0-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ff0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="05ff0-106">Ez egy súgó parancsmag, amely egy támogatási jegy létrehozásakor vagy frissítésekénél használható támogatási kapcsolatprofil-objektum létrehozásához használható.</span><span class="sxs-lookup"><span data-stu-id="05ff0-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="05ff0-107">Meg kell adnia az alábbi paramétereket, amelyek kötelezőek a támogatási jegy létrehozásához:</span><span class="sxs-lookup"><span data-stu-id="05ff0-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="05ff0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05ff0-108">EXAMPLES</span></span>

### <span data-ttu-id="05ff0-109">1. példa: Névjegyobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="05ff0-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="05ff0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05ff0-110">PARAMETERS</span></span>

### <span data-ttu-id="05ff0-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="05ff0-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="05ff0-112">Az itt felsorolt e-mail-címeket a rendszer a támogatási jegyről küldött minden levélre átmásolja.</span><span class="sxs-lookup"><span data-stu-id="05ff0-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="05ff0-113">-Country</span><span class="sxs-lookup"><span data-stu-id="05ff0-113">-Country</span></span>
<span data-ttu-id="05ff0-114">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="05ff0-114">Customer country.</span></span>
<span data-ttu-id="05ff0-115">Érvényes ISO Alfa-3 országkódnak (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="05ff0-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="05ff0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ff0-116">-DefaultProfile</span></span>
<span data-ttu-id="05ff0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05ff0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ff0-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="05ff0-118">-FirstName</span></span>
<span data-ttu-id="05ff0-119">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="05ff0-119">Customer first name.</span></span>

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

### <span data-ttu-id="05ff0-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="05ff0-120">-LastName</span></span>
<span data-ttu-id="05ff0-121">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="05ff0-121">Customer last name.</span></span>

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

### <span data-ttu-id="05ff0-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="05ff0-122">-PhoneNumber</span></span>
<span data-ttu-id="05ff0-123">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="05ff0-123">Customer phone number.</span></span>
<span data-ttu-id="05ff0-124">Erre akkor van szükség, ha az előnyben részesített kapcsolatfelvételi mód a telefon.</span><span class="sxs-lookup"><span data-stu-id="05ff0-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="05ff0-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="05ff0-125">-PreferredContactMethod</span></span>
<span data-ttu-id="05ff0-126">Előnyben részesített kapcsolatfelvételi mód.</span><span class="sxs-lookup"><span data-stu-id="05ff0-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="05ff0-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="05ff0-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="05ff0-128">Az ügyfél elsődleges támogatási nyelve.</span><span class="sxs-lookup"><span data-stu-id="05ff0-128">Customer preferred support language.</span></span>
<span data-ttu-id="05ff0-129">A kódnak érvényesnek kell lennie az itt felsorolt nyelvek https://azure.microsoft.com/support/faq/ egyikében.</span><span class="sxs-lookup"><span data-stu-id="05ff0-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="05ff0-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="05ff0-130">-PreferredTimeZone</span></span>
<span data-ttu-id="05ff0-131">Ügyfél által előnyben részesített időzóna.</span><span class="sxs-lookup"><span data-stu-id="05ff0-131">Customer preferred time zone.</span></span>
<span data-ttu-id="05ff0-132">Ennek érvényes System.TimeZoneInfo.Id kell lennie.</span><span class="sxs-lookup"><span data-stu-id="05ff0-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="05ff0-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="05ff0-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="05ff0-134">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="05ff0-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="05ff0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05ff0-135">-Confirm</span></span>
<span data-ttu-id="05ff0-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05ff0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ff0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ff0-137">-WhatIf</span></span>
<span data-ttu-id="05ff0-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05ff0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ff0-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05ff0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ff0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ff0-140">CommonParameters</span></span>
<span data-ttu-id="05ff0-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ff0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ff0-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05ff0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ff0-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05ff0-143">INPUTS</span></span>

### <span data-ttu-id="05ff0-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="05ff0-144">None</span></span>

## <span data-ttu-id="05ff0-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05ff0-145">OUTPUTS</span></span>

### <span data-ttu-id="05ff0-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="05ff0-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="05ff0-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05ff0-147">NOTES</span></span>

## <span data-ttu-id="05ff0-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05ff0-148">RELATED LINKS</span></span>
