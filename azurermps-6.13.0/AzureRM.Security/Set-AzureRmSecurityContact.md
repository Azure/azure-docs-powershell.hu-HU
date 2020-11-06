---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495659"
---
# <span data-ttu-id="6ca88-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="6ca88-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="6ca88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ca88-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca88-103">Az előfizetéshez tartozó biztonsági partnerek frissítése</span><span class="sxs-lookup"><span data-stu-id="6ca88-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ca88-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca88-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ca88-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca88-106">Az előfizetéshez tartozó biztonsági partnerek frissítése</span><span class="sxs-lookup"><span data-stu-id="6ca88-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="6ca88-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6ca88-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca88-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ca88-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="6ca88-109">Az előfizetéshez tartozó biztonsági partnerek frissítése</span><span class="sxs-lookup"><span data-stu-id="6ca88-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="6ca88-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ca88-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca88-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="6ca88-111">-AlertAdmin</span></span>
<span data-ttu-id="6ca88-112">Riasztások a rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="6ca88-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca88-113">-DefaultProfile</span></span>
<span data-ttu-id="6ca88-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ca88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-115">– E-mail</span><span class="sxs-lookup"><span data-stu-id="6ca88-115">-Email</span></span>
<span data-ttu-id="6ca88-116">E-mail.</span><span class="sxs-lookup"><span data-stu-id="6ca88-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ca88-117">-Name</span></span>
<span data-ttu-id="6ca88-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="6ca88-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="6ca88-119">-NotifyOnAlert</span></span>
<span data-ttu-id="6ca88-120">Riasztási értesítések.</span><span class="sxs-lookup"><span data-stu-id="6ca88-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="6ca88-121">-Phone</span></span>
<span data-ttu-id="6ca88-122">Phone.</span><span class="sxs-lookup"><span data-stu-id="6ca88-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ca88-123">-Confirm</span></span>
<span data-ttu-id="6ca88-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ca88-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca88-125">-WhatIf</span></span>
<span data-ttu-id="6ca88-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ca88-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ca88-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ca88-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca88-128">CommonParameters</span></span>
<span data-ttu-id="6ca88-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ca88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca88-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca88-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ca88-131">INPUTS</span></span>

### <span data-ttu-id="6ca88-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca88-132">System.String</span></span>

## <span data-ttu-id="6ca88-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ca88-133">OUTPUTS</span></span>

### <span data-ttu-id="6ca88-134">Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="6ca88-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="6ca88-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ca88-135">NOTES</span></span>

## <span data-ttu-id="6ca88-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ca88-136">RELATED LINKS</span></span>
