---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015820"
---
# <span data-ttu-id="65545-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65545-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="65545-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65545-102">SYNOPSIS</span></span>
<span data-ttu-id="65545-103">Frissíti a meglévő szolgáltatás-busz engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="65545-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="65545-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65545-104">SYNTAX</span></span>

### <span data-ttu-id="65545-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="65545-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65545-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="65545-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65545-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="65545-107">DESCRIPTION</span></span>
<span data-ttu-id="65545-108">Frissíti a meglévő szolgáltatás-busz engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="65545-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="65545-109">Példák</span><span class="sxs-lookup"><span data-stu-id="65545-109">EXAMPLES</span></span>

### <span data-ttu-id="65545-110">1. példa: engedélyezési szabály elsődleges kulcsának megújítása a névtér szintjén</span><span class="sxs-lookup"><span data-stu-id="65545-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="65545-111">Az elsődleges kulcs megújult.</span><span class="sxs-lookup"><span data-stu-id="65545-111">The primary key is renewed.</span></span>

### <span data-ttu-id="65545-112">2. példa: az engedélyezési szabály engedélyeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="65545-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="65545-113">Frissíti az engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="65545-113">Updates the permissions.</span></span>

## <span data-ttu-id="65545-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65545-114">PARAMETERS</span></span>

### <span data-ttu-id="65545-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="65545-115">-EntityName</span></span>
<span data-ttu-id="65545-116">Az entitás neve, amelyre a szabályt alkalmazni kell.</span><span class="sxs-lookup"><span data-stu-id="65545-116">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65545-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="65545-117">-EntityType</span></span>
<span data-ttu-id="65545-118">Az egyed típusa (várólista, témakör, továbbítás, NotificationHub)</span><span class="sxs-lookup"><span data-stu-id="65545-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65545-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65545-119">-Name</span></span>
<span data-ttu-id="65545-120">Az egyedi engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="65545-120">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65545-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65545-121">-Namespace</span></span>
<span data-ttu-id="65545-122">A névtér neve az engedélyezési szabály alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="65545-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="65545-123">Ha nincs EntityName, feltéve, hogy a szabály a névtér szintjén lesz.</span><span class="sxs-lookup"><span data-stu-id="65545-123">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65545-124">– Engedély</span><span class="sxs-lookup"><span data-stu-id="65545-124">-Permission</span></span>
<span data-ttu-id="65545-125">Az engedélyezési engedélyek (küldés, kezelés, figyelés)</span><span class="sxs-lookup"><span data-stu-id="65545-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65545-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="65545-126">-PrimaryKey</span></span>
<span data-ttu-id="65545-127">A megosztott hozzáférés aláírása elsődleges kulcs.</span><span class="sxs-lookup"><span data-stu-id="65545-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="65545-128">Akkor fog létrejönni, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="65545-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65545-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="65545-129">-Profile</span></span>
<span data-ttu-id="65545-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="65545-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65545-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="65545-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65545-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="65545-132">-SecondaryKey</span></span>
<span data-ttu-id="65545-133">A megosztott hozzáférés-aláírás másodlagos kulcsa.</span><span class="sxs-lookup"><span data-stu-id="65545-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65545-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65545-134">CommonParameters</span></span>
<span data-ttu-id="65545-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65545-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65545-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65545-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65545-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65545-137">INPUTS</span></span>

## <span data-ttu-id="65545-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65545-138">OUTPUTS</span></span>

## <span data-ttu-id="65545-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65545-139">NOTES</span></span>

## <span data-ttu-id="65545-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65545-140">RELATED LINKS</span></span>

[<span data-ttu-id="65545-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65545-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="65545-142">Új – AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65545-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="65545-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65545-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


