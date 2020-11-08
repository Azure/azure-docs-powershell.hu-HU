---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186058"
---
# <span data-ttu-id="b5bf1-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="b5bf1-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="b5bf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bf1-103">Az értesítési hub engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="b5bf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5bf1-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5bf1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="b5bf1-106">A **Get-AzNotificationHubListKey** parancsmag az értesítési hub megosztott elérésű aláírás-engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="b5bf1-107">Az engedélyezési szabályok a jogosultságokat kezelik a hub számára.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="b5bf1-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="b5bf1-109">Ezek a kapcsolati karakterláncok (URI-k) a következőket végezzék el:</span><span class="sxs-lookup"><span data-stu-id="b5bf1-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="b5bf1-110">A felhasználók rámutatnak egy erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-110">Point users to a resource.</span></span>
- <span data-ttu-id="b5bf1-111">Lekérdezési paramétereket tartalmazó jogkivonat felvétele</span><span class="sxs-lookup"><span data-stu-id="b5bf1-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="b5bf1-112">Az alábbi paraméterek közül az aláírás a felhasználó hitelesítésére szolgál, és megadja a megadott szintű hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="b5bf1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b5bf1-113">EXAMPLES</span></span>

### <span data-ttu-id="b5bf1-114">Példa 1: az elsődleges és másodlagos kapcsolati karakterláncok beszerzése egy engedélyezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="b5bf1-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b5bf1-115">Ez a parancs beolvassa az elsődleges és másodlagos kapcsolati karakterláncot az engedélyezési szabály ListenRule, amely az ContosoInternalHub értesítési központhoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="b5bf1-116">A parancsnak tartalmaznia kell a hub névteret és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="b5bf1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5bf1-117">PARAMETERS</span></span>

### <span data-ttu-id="b5bf1-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5bf1-118">-AuthorizationRule</span></span>
<span data-ttu-id="b5bf1-119">A megosztott hozzáférés-aláírások (SAS) hitelesítési szabályának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="b5bf1-120">Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="b5bf1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bf1-121">-DefaultProfile</span></span>
<span data-ttu-id="b5bf1-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5bf1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5bf1-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5bf1-123">-Namespace</span></span>
<span data-ttu-id="b5bf1-124">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="b5bf1-125">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b5bf1-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b5bf1-126">-NotificationHub</span></span>
<span data-ttu-id="b5bf1-127">Megadja azt az értesítési központot, amely a parancsmag engedélyezési szabályát rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="b5bf1-128">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="b5bf1-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5bf1-129">-ResourceGroup</span></span>
<span data-ttu-id="b5bf1-130">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="b5bf1-131">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="b5bf1-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b5bf1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bf1-132">CommonParameters</span></span>
<span data-ttu-id="b5bf1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5bf1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bf1-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5bf1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bf1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5bf1-135">INPUTS</span></span>

### <span data-ttu-id="b5bf1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b5bf1-136">System.String</span></span>

## <span data-ttu-id="b5bf1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5bf1-137">OUTPUTS</span></span>

### <span data-ttu-id="b5bf1-138">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="b5bf1-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="b5bf1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5bf1-139">NOTES</span></span>

## <span data-ttu-id="b5bf1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5bf1-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5bf1-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5bf1-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


