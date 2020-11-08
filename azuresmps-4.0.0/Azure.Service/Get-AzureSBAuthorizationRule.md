---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015614"
---
# <span data-ttu-id="481d1-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="481d1-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="481d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="481d1-102">SYNOPSIS</span></span>
<span data-ttu-id="481d1-103">A szolgáltatás busz-engedélyezési szabályait kapja.</span><span class="sxs-lookup"><span data-stu-id="481d1-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="481d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="481d1-104">SYNTAX</span></span>

### <span data-ttu-id="481d1-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="481d1-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="481d1-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="481d1-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="481d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="481d1-107">DESCRIPTION</span></span>
<span data-ttu-id="481d1-108">A szolgáltatás busz-engedélyezési szabályait kapja.</span><span class="sxs-lookup"><span data-stu-id="481d1-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="481d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="481d1-109">EXAMPLES</span></span>

### <span data-ttu-id="481d1-110">1. példa: engedélyezési szabály kérése a névtér szintjén</span><span class="sxs-lookup"><span data-stu-id="481d1-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="481d1-111">Az összes rendelkezésre álló engedélyezési szabály a MyNamespace címen szerezhető be.</span><span class="sxs-lookup"><span data-stu-id="481d1-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="481d1-112">2. példa: engedélyezési szabály kérése egy várólistához</span><span class="sxs-lookup"><span data-stu-id="481d1-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="481d1-113">Az összes rendelkezésre álló engedélyezési szabály egy MyEntity-várólistára kerül a MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="481d1-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="481d1-114">3. példa: engedélyezési szabály kérése név szerint</span><span class="sxs-lookup"><span data-stu-id="481d1-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="481d1-115">A MyRule nevű engedélyezési szabályt MyNamespace szinten kapja.</span><span class="sxs-lookup"><span data-stu-id="481d1-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="481d1-116">4. példa: engedélyezési szabály kérése engedély szerint</span><span class="sxs-lookup"><span data-stu-id="481d1-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="481d1-117">Megkapja az összes olyan engedélyezési szabályt, amely a névtér szintjén küldi el az engedélyt.</span><span class="sxs-lookup"><span data-stu-id="481d1-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="481d1-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="481d1-118">PARAMETERS</span></span>

### <span data-ttu-id="481d1-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="481d1-119">-EntityName</span></span>
<span data-ttu-id="481d1-120">Az entitás neve, amelyre a szabályt alkalmazni kell.</span><span class="sxs-lookup"><span data-stu-id="481d1-120">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="481d1-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="481d1-121">-EntityType</span></span>
<span data-ttu-id="481d1-122">Az egyed típusa (várólista, témakör, továbbítás, NotificationHub)</span><span class="sxs-lookup"><span data-stu-id="481d1-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="481d1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="481d1-123">-Name</span></span>
<span data-ttu-id="481d1-124">Az egyedi engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="481d1-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481d1-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="481d1-125">-Namespace</span></span>
<span data-ttu-id="481d1-126">A névtér neve az engedélyezési szabály alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="481d1-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="481d1-127">Ha nincs EntityName, feltéve, hogy a szabály a névtér szintjén lesz.</span><span class="sxs-lookup"><span data-stu-id="481d1-127">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="481d1-128">– Engedély</span><span class="sxs-lookup"><span data-stu-id="481d1-128">-Permission</span></span>
<span data-ttu-id="481d1-129">A szűrés (küldés, kezelés, figyelés) engedélyezési engedélyei.</span><span class="sxs-lookup"><span data-stu-id="481d1-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="481d1-130">Ez a pontos egyezést használja.</span><span class="sxs-lookup"><span data-stu-id="481d1-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481d1-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="481d1-131">-Profile</span></span>
<span data-ttu-id="481d1-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="481d1-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="481d1-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="481d1-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="481d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481d1-134">CommonParameters</span></span>
<span data-ttu-id="481d1-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="481d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481d1-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="481d1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481d1-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="481d1-137">INPUTS</span></span>

## <span data-ttu-id="481d1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="481d1-138">OUTPUTS</span></span>

## <span data-ttu-id="481d1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="481d1-139">NOTES</span></span>

## <span data-ttu-id="481d1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="481d1-140">RELATED LINKS</span></span>

[<span data-ttu-id="481d1-141">Új – AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="481d1-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="481d1-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="481d1-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="481d1-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="481d1-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


