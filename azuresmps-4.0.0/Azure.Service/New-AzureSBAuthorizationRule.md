---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015987"
---
# <span data-ttu-id="d5edb-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5edb-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="d5edb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5edb-102">SYNOPSIS</span></span>
<span data-ttu-id="d5edb-103">Új szolgáltatási busz engedélyezési szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d5edb-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="d5edb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5edb-104">SYNTAX</span></span>

### <span data-ttu-id="d5edb-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="d5edb-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d5edb-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="d5edb-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5edb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5edb-107">DESCRIPTION</span></span>
<span data-ttu-id="d5edb-108">A **New-AzureSBAuthorizationRule** parancsmag létrehoz egy szolgáltatási busz engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="d5edb-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="d5edb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5edb-109">EXAMPLES</span></span>

### <span data-ttu-id="d5edb-110">Példa 1: engedélyezési szabály létrehozása a generált elsődleges kulccsal</span><span class="sxs-lookup"><span data-stu-id="d5edb-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="d5edb-111">Új engedélyezési szabály létrehozása a névtér szintjén a küldési engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="d5edb-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="d5edb-112">2. példa: engedélyezési szabály létrehozása az elsődleges kulcs megadásával</span><span class="sxs-lookup"><span data-stu-id="d5edb-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="d5edb-113">Új engedélyezési szabályt hoz létre a MyEntity-várólistán az összes engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="d5edb-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="d5edb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5edb-114">PARAMETERS</span></span>

### <span data-ttu-id="d5edb-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="d5edb-115">-EntityName</span></span>
<span data-ttu-id="d5edb-116">Annak a szervezetnek a nevét adja meg, amelyre a szabályt alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="d5edb-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5edb-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="d5edb-117">-EntityType</span></span>
<span data-ttu-id="d5edb-118">Az egyed típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5edb-118">Specifies the entity type.</span></span>
<span data-ttu-id="d5edb-119">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d5edb-119">Valid values are:</span></span>
  
- <span data-ttu-id="d5edb-120">Várólista</span><span class="sxs-lookup"><span data-stu-id="d5edb-120">Queue</span></span>
- <span data-ttu-id="d5edb-121">Témakör</span><span class="sxs-lookup"><span data-stu-id="d5edb-121">Topic</span></span>
- <span data-ttu-id="d5edb-122">Relé</span><span class="sxs-lookup"><span data-stu-id="d5edb-122">Relay</span></span>
- <span data-ttu-id="d5edb-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d5edb-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5edb-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5edb-124">-Name</span></span>
<span data-ttu-id="d5edb-125">Az egyedi engedélyezési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5edb-125">Specifies the unique authorization rule name.</span></span>

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

### <span data-ttu-id="d5edb-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d5edb-126">-Namespace</span></span>
<span data-ttu-id="d5edb-127">Annak a névtérnek a nevét adja meg, amely az engedélyezési szabályt alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="d5edb-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="d5edb-128">Ha nincs *EntityName* , feltéve, hogy a szabály a névtér szintjén lesz.</span><span class="sxs-lookup"><span data-stu-id="d5edb-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="d5edb-129">– Engedély</span><span class="sxs-lookup"><span data-stu-id="d5edb-129">-Permission</span></span>
<span data-ttu-id="d5edb-130">Az engedélyezési engedélyek (küldés, kezelés, figyelés)</span><span class="sxs-lookup"><span data-stu-id="d5edb-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="d5edb-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d5edb-131">-PrimaryKey</span></span>
<span data-ttu-id="d5edb-132">A megosztott hozzáférés-aláírás elsődleges kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5edb-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="d5edb-133">Akkor fog létrejönni, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d5edb-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="d5edb-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5edb-134">-Profile</span></span>
<span data-ttu-id="d5edb-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d5edb-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5edb-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d5edb-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5edb-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d5edb-137">-SecondaryKey</span></span>
<span data-ttu-id="d5edb-138">A megosztott hozzáférés-aláírás másodlagos kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5edb-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="d5edb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5edb-139">CommonParameters</span></span>
<span data-ttu-id="d5edb-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5edb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5edb-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5edb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5edb-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5edb-142">INPUTS</span></span>

## <span data-ttu-id="d5edb-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5edb-143">OUTPUTS</span></span>

## <span data-ttu-id="d5edb-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5edb-144">NOTES</span></span>

## <span data-ttu-id="d5edb-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5edb-145">RELATED LINKS</span></span>

[<span data-ttu-id="d5edb-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5edb-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d5edb-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5edb-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d5edb-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5edb-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


