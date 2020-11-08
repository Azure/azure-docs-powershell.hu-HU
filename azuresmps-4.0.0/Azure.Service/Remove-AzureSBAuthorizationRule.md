---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016131"
---
# <span data-ttu-id="96510-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96510-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="96510-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96510-102">SYNOPSIS</span></span>
<span data-ttu-id="96510-103">Eltávolítja a meglévő szolgáltatás-busz engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="96510-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="96510-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96510-104">SYNTAX</span></span>

### <span data-ttu-id="96510-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="96510-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="96510-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="96510-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="96510-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="96510-107">DESCRIPTION</span></span>
<span data-ttu-id="96510-108">Eltávolítja a meglévő szolgáltatás-busz engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="96510-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="96510-109">Példák</span><span class="sxs-lookup"><span data-stu-id="96510-109">EXAMPLES</span></span>

### <span data-ttu-id="96510-110">Példa 1: engedélyezési szabály eltávolítása a névtér szintjén</span><span class="sxs-lookup"><span data-stu-id="96510-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="96510-111">Eltávolítja az engedélyezési szabály MyRule a MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="96510-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="96510-112">2. példa: a várólista engedélyezési szabályának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="96510-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="96510-113">Eltávolítja az MyNamespace nevű MyEntity-várólistára vonatkozó MyRule nevű engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="96510-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="96510-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96510-114">PARAMETERS</span></span>

### <span data-ttu-id="96510-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="96510-115">-EntityName</span></span>
<span data-ttu-id="96510-116">Az entitás neve, amelyre a szabályt alkalmazni kell.</span><span class="sxs-lookup"><span data-stu-id="96510-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="96510-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="96510-117">-EntityType</span></span>
<span data-ttu-id="96510-118">Az egyed típusa (várólista, témakör, továbbítás, NotificationHub)</span><span class="sxs-lookup"><span data-stu-id="96510-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="96510-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96510-119">-Name</span></span>
<span data-ttu-id="96510-120">Az egyedi engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="96510-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="96510-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="96510-121">-Namespace</span></span>
<span data-ttu-id="96510-122">A névtér neve az engedélyezési szabály alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="96510-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="96510-123">Ha nincs EntityName, feltéve, hogy a szabály a névtér szintjén lesz.</span><span class="sxs-lookup"><span data-stu-id="96510-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="96510-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96510-124">-PassThru</span></span>
<span data-ttu-id="96510-125">Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="96510-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="96510-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="96510-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96510-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="96510-127">-Profile</span></span>
<span data-ttu-id="96510-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="96510-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96510-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="96510-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96510-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96510-130">CommonParameters</span></span>
<span data-ttu-id="96510-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96510-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96510-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96510-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96510-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96510-133">INPUTS</span></span>

## <span data-ttu-id="96510-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96510-134">OUTPUTS</span></span>

## <span data-ttu-id="96510-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96510-135">NOTES</span></span>

## <span data-ttu-id="96510-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96510-136">RELATED LINKS</span></span>

[<span data-ttu-id="96510-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96510-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="96510-138">Új – AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96510-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="96510-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96510-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


