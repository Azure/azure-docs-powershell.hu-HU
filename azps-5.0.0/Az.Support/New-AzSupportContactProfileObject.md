---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185165"
---
# <span data-ttu-id="447fd-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="447fd-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="447fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="447fd-102">SYNOPSIS</span></span>
<span data-ttu-id="447fd-103">Egy támogatási partnercsoport-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="447fd-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="447fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="447fd-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447fd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="447fd-105">DESCRIPTION</span></span>
<span data-ttu-id="447fd-106">Ez egy olyan segítő parancsmag, amellyel támogatási jegy létrehozásakor vagy frissítésekor létrehozhatja az ügyfélszolgálati profil objektumát.</span><span class="sxs-lookup"><span data-stu-id="447fd-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="447fd-107">A támogatási jegy létrehozásához kötelezően meg kell adnia az alábbi paramétereket:</span><span class="sxs-lookup"><span data-stu-id="447fd-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="447fd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="447fd-108">EXAMPLES</span></span>

### <span data-ttu-id="447fd-109">1. példa: Partnercsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="447fd-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="447fd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="447fd-110">PARAMETERS</span></span>

### <span data-ttu-id="447fd-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="447fd-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="447fd-112">Az itt felsorolt e-mail-címeket a támogatási jegyre vonatkozó minden levelezésre másolhatja.</span><span class="sxs-lookup"><span data-stu-id="447fd-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="447fd-113">-Ország</span><span class="sxs-lookup"><span data-stu-id="447fd-113">-Country</span></span>
<span data-ttu-id="447fd-114">Ügyfél országa.</span><span class="sxs-lookup"><span data-stu-id="447fd-114">Customer country.</span></span>
<span data-ttu-id="447fd-115">A kódnak érvényes ISO Alpha-3 országkód (ISO 3166) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="447fd-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="447fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447fd-116">-DefaultProfile</span></span>
<span data-ttu-id="447fd-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="447fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="447fd-118">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="447fd-118">-FirstName</span></span>
<span data-ttu-id="447fd-119">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="447fd-119">Customer first name.</span></span>

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

### <span data-ttu-id="447fd-120">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="447fd-120">-LastName</span></span>
<span data-ttu-id="447fd-121">Ügyfél vezetékneve.</span><span class="sxs-lookup"><span data-stu-id="447fd-121">Customer last name.</span></span>

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

### <span data-ttu-id="447fd-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="447fd-122">-PhoneNumber</span></span>
<span data-ttu-id="447fd-123">Ügyfél telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="447fd-123">Customer phone number.</span></span>
<span data-ttu-id="447fd-124">Erre akkor van szükség, ha az elsődleges névjegykártya-módszer telefon.</span><span class="sxs-lookup"><span data-stu-id="447fd-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="447fd-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="447fd-125">-PreferredContactMethod</span></span>
<span data-ttu-id="447fd-126">Preferált kontakt mód</span><span class="sxs-lookup"><span data-stu-id="447fd-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="447fd-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="447fd-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="447fd-128">Az ügyfél által előnyben részesített támogatási nyelv.</span><span class="sxs-lookup"><span data-stu-id="447fd-128">Customer preferred support language.</span></span>
<span data-ttu-id="447fd-129">Ennek az itt felsorolt támogatott nyelvek egyikéhez érvényes célnyelv-kódnak kell lennie https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="447fd-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="447fd-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="447fd-130">-PreferredTimeZone</span></span>
<span data-ttu-id="447fd-131">Ügyfél által preferált időzóna</span><span class="sxs-lookup"><span data-stu-id="447fd-131">Customer preferred time zone.</span></span>
<span data-ttu-id="447fd-132">Ennek érvényes System.TimeZoneInfo.Id-értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="447fd-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="447fd-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="447fd-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="447fd-134">Ügyfél elsődleges e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="447fd-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="447fd-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="447fd-135">-Confirm</span></span>
<span data-ttu-id="447fd-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="447fd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="447fd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="447fd-137">-WhatIf</span></span>
<span data-ttu-id="447fd-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="447fd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="447fd-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="447fd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="447fd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447fd-140">CommonParameters</span></span>
<span data-ttu-id="447fd-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="447fd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447fd-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="447fd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447fd-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="447fd-143">INPUTS</span></span>

### <span data-ttu-id="447fd-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="447fd-144">None</span></span>

## <span data-ttu-id="447fd-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="447fd-145">OUTPUTS</span></span>

### <span data-ttu-id="447fd-146">Microsoft. Azure. commands. support. models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="447fd-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="447fd-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="447fd-147">NOTES</span></span>

## <span data-ttu-id="447fd-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="447fd-148">RELATED LINKS</span></span>