---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 1bf9e6b51899054899e819784872cf688a182e16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669224"
---
# <span data-ttu-id="07abb-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="07abb-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="07abb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07abb-102">SYNOPSIS</span></span>
<span data-ttu-id="07abb-103">Az előfizetéshez tartozó biztonsági partnerek frissítése</span><span class="sxs-lookup"><span data-stu-id="07abb-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="07abb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07abb-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07abb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07abb-105">DESCRIPTION</span></span>
<span data-ttu-id="07abb-106">Az előfizetéshez tartozó biztonsági partnerek frissítése</span><span class="sxs-lookup"><span data-stu-id="07abb-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="07abb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="07abb-107">EXAMPLES</span></span>

### <span data-ttu-id="07abb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07abb-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="07abb-109">Az előfizetéshez tartozó biztonsági partnerek frissítése</span><span class="sxs-lookup"><span data-stu-id="07abb-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="07abb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07abb-110">PARAMETERS</span></span>

### <span data-ttu-id="07abb-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="07abb-111">-AlertAdmin</span></span>
<span data-ttu-id="07abb-112">Riasztások a rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="07abb-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="07abb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07abb-113">-DefaultProfile</span></span>
<span data-ttu-id="07abb-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07abb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07abb-115">– E-mail</span><span class="sxs-lookup"><span data-stu-id="07abb-115">-Email</span></span>
<span data-ttu-id="07abb-116">E-mail.</span><span class="sxs-lookup"><span data-stu-id="07abb-116">E-Mail.</span></span>

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

### <span data-ttu-id="07abb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07abb-117">-Name</span></span>
<span data-ttu-id="07abb-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="07abb-118">Resource name.</span></span>

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

### <span data-ttu-id="07abb-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="07abb-119">-NotifyOnAlert</span></span>
<span data-ttu-id="07abb-120">Riasztási értesítések.</span><span class="sxs-lookup"><span data-stu-id="07abb-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="07abb-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="07abb-121">-Phone</span></span>
<span data-ttu-id="07abb-122">Phone.</span><span class="sxs-lookup"><span data-stu-id="07abb-122">Phone.</span></span>

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

### <span data-ttu-id="07abb-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07abb-123">-Confirm</span></span>
<span data-ttu-id="07abb-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07abb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07abb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07abb-125">-WhatIf</span></span>
<span data-ttu-id="07abb-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07abb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07abb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07abb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07abb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07abb-128">CommonParameters</span></span>
<span data-ttu-id="07abb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07abb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07abb-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07abb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07abb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07abb-131">INPUTS</span></span>

### <span data-ttu-id="07abb-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="07abb-132">None</span></span>

## <span data-ttu-id="07abb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07abb-133">OUTPUTS</span></span>

### <span data-ttu-id="07abb-134">Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="07abb-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="07abb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07abb-135">NOTES</span></span>

## <span data-ttu-id="07abb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07abb-136">RELATED LINKS</span></span>
