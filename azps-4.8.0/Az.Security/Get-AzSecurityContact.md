---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180905"
---
# <span data-ttu-id="a066e-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a066e-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="a066e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a066e-102">SYNOPSIS</span></span>
<span data-ttu-id="a066e-103">Az előfizetésben konfigurált biztonsági névjegyek lekérdezése</span><span class="sxs-lookup"><span data-stu-id="a066e-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="a066e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a066e-104">SYNTAX</span></span>

### <span data-ttu-id="a066e-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a066e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a066e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a066e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a066e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a066e-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a066e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a066e-108">DESCRIPTION</span></span>
<span data-ttu-id="a066e-109">Megkapja az előfizetésben konfigurált biztonsági névjegyeket.</span><span class="sxs-lookup"><span data-stu-id="a066e-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="a066e-110">A biztonsági partnerek értesítést kaphatnak az előfizetésben megjelenő biztonsági figyelmeztetésekről.</span><span class="sxs-lookup"><span data-stu-id="a066e-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="a066e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a066e-111">EXAMPLES</span></span>

### <span data-ttu-id="a066e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a066e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a066e-113">Az összes konfigurált biztonsági partner beolvasása az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="a066e-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="a066e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a066e-114">PARAMETERS</span></span>

### <span data-ttu-id="a066e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a066e-115">-DefaultProfile</span></span>
<span data-ttu-id="a066e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a066e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a066e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a066e-117">-Name</span></span>
<span data-ttu-id="a066e-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a066e-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a066e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a066e-119">-ResourceId</span></span>
<span data-ttu-id="a066e-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a066e-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a066e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a066e-121">CommonParameters</span></span>
<span data-ttu-id="a066e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a066e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a066e-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a066e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a066e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a066e-124">INPUTS</span></span>

### <span data-ttu-id="a066e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a066e-125">System.String</span></span>

## <span data-ttu-id="a066e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a066e-126">OUTPUTS</span></span>

### <span data-ttu-id="a066e-127">Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a066e-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a066e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a066e-128">NOTES</span></span>

## <span data-ttu-id="a066e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a066e-129">RELATED LINKS</span></span>
