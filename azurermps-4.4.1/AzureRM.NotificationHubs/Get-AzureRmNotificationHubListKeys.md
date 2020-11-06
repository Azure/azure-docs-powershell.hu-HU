---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 924b729ca8ba324a6f44cade48ed803b2867b6b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504808"
---
# <span data-ttu-id="e97ca-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="e97ca-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="e97ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e97ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e97ca-103">Az értesítési hub engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e97ca-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e97ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e97ca-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e97ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e97ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e97ca-106">A **Get-AzureRmNotificationHubListKeys** parancsmag az értesítési hub megosztott elérésű aláírás-engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e97ca-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="e97ca-107">Az engedélyezési szabályok a jogosultságokat kezelik a hub számára.</span><span class="sxs-lookup"><span data-stu-id="e97ca-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="e97ca-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="e97ca-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="e97ca-109">Ezek a kapcsolati karakterláncok (URI-k) a következőket végezzék el:</span><span class="sxs-lookup"><span data-stu-id="e97ca-109">These connection strings (URIs) perform the following:</span></span>

- <span data-ttu-id="e97ca-110">A felhasználók rámutatnak egy erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="e97ca-110">Point users to a resource.</span></span>
- <span data-ttu-id="e97ca-111">Lekérdezési paramétereket tartalmazó jogkivonat felvétele</span><span class="sxs-lookup"><span data-stu-id="e97ca-111">Include a token containing query parameters.</span></span>

<span data-ttu-id="e97ca-112">Az alábbi paraméterek közül az aláírás a felhasználó hitelesítésére szolgál, és megadja a megadott szintű hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="e97ca-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="e97ca-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e97ca-113">EXAMPLES</span></span>

### <span data-ttu-id="e97ca-114">Példa 1: az elsődleges és másodlagos kapcsolati karakterláncok beszerzése egy engedélyezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="e97ca-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="e97ca-115">Ez a parancs beolvassa az elsődleges és másodlagos kapcsolati karakterláncot az engedélyezési szabály ListenRule, amely az ContosoInternalHub értesítési központhoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e97ca-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="e97ca-116">A parancsnak tartalmaznia kell a hub névteret és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="e97ca-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="e97ca-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e97ca-117">PARAMETERS</span></span>

### <span data-ttu-id="e97ca-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e97ca-118">-AuthorizationRule</span></span>
<span data-ttu-id="e97ca-119">A megosztott hozzáférés-aláírások (SAS) hitelesítési szabályának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e97ca-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="e97ca-120">Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="e97ca-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97ca-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e97ca-121">-Namespace</span></span>
<span data-ttu-id="e97ca-122">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e97ca-122">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="e97ca-123">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="e97ca-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97ca-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e97ca-124">-NotificationHub</span></span>
<span data-ttu-id="e97ca-125">Megadja azt az értesítési központot, amely a parancsmag engedélyezési szabályát rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="e97ca-125">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="e97ca-126">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="e97ca-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97ca-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e97ca-127">-ResourceGroup</span></span>
<span data-ttu-id="e97ca-128">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e97ca-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="e97ca-129">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="e97ca-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97ca-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97ca-130">-DefaultProfile</span></span>
<span data-ttu-id="e97ca-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e97ca-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e97ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97ca-132">CommonParameters</span></span>
<span data-ttu-id="e97ca-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e97ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97ca-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e97ca-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97ca-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e97ca-135">INPUTS</span></span>

## <span data-ttu-id="e97ca-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e97ca-136">OUTPUTS</span></span>

### <span data-ttu-id="e97ca-137">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="e97ca-137">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="e97ca-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e97ca-138">NOTES</span></span>

## <span data-ttu-id="e97ca-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e97ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="e97ca-140">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e97ca-140">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


