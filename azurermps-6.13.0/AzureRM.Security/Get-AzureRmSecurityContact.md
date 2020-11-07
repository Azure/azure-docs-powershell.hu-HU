---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679508"
---
# <span data-ttu-id="c91d2-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="c91d2-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="c91d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c91d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c91d2-103">Az előfizetésben konfigurált biztonsági névjegyek lekérdezése</span><span class="sxs-lookup"><span data-stu-id="c91d2-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c91d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c91d2-104">SYNTAX</span></span>

### <span data-ttu-id="c91d2-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c91d2-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c91d2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c91d2-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c91d2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c91d2-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c91d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c91d2-108">DESCRIPTION</span></span>
<span data-ttu-id="c91d2-109">Megkapja az előfizetésben konfigurált biztonsági névjegyeket.</span><span class="sxs-lookup"><span data-stu-id="c91d2-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="c91d2-110">A biztonsági partnerek értesítést kaphatnak az előfizetésben megjelenő biztonsági figyelmeztetésekről.</span><span class="sxs-lookup"><span data-stu-id="c91d2-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="c91d2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c91d2-111">EXAMPLES</span></span>

### <span data-ttu-id="c91d2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c91d2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="c91d2-113">Az összes konfigurált biztonsági partner beolvasása az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="c91d2-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="c91d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c91d2-114">PARAMETERS</span></span>

### <span data-ttu-id="c91d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91d2-115">-DefaultProfile</span></span>
<span data-ttu-id="c91d2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c91d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c91d2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c91d2-117">-Name</span></span>
<span data-ttu-id="c91d2-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="c91d2-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c91d2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c91d2-119">-ResourceId</span></span>
<span data-ttu-id="c91d2-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c91d2-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91d2-121">CommonParameters</span></span>
<span data-ttu-id="c91d2-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c91d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91d2-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c91d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91d2-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c91d2-124">INPUTS</span></span>

### <span data-ttu-id="c91d2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c91d2-125">System.String</span></span>

## <span data-ttu-id="c91d2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c91d2-126">OUTPUTS</span></span>

### <span data-ttu-id="c91d2-127">Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="c91d2-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="c91d2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c91d2-128">NOTES</span></span>

## <span data-ttu-id="c91d2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c91d2-129">RELATED LINKS</span></span>
