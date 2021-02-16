---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146531"
---
# <span data-ttu-id="35248-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="35248-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="35248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35248-102">SYNOPSIS</span></span>
<span data-ttu-id="35248-103">Egy értesítési központ engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="35248-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="35248-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35248-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35248-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35248-105">DESCRIPTION</span></span>
<span data-ttu-id="35248-106">A **Get-AzNotificationHubListKey** parancsmag egy értesítési központ Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="35248-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="35248-107">Az engedélyezési szabályok kezelik a felhasználói jogokat a központban.</span><span class="sxs-lookup"><span data-stu-id="35248-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="35248-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="35248-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="35248-109">Az alábbi kapcsolati karakterláncok (URI-k) az alábbi műveleteket hajtják végre:</span><span class="sxs-lookup"><span data-stu-id="35248-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="35248-110">Mutasson a felhasználóknak egy erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="35248-110">Point users to a resource.</span></span>
- <span data-ttu-id="35248-111">Lekérdezésparamétereket tartalmazó jogkivonatot is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="35248-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="35248-112">A paraméterek egyike, az aláírás a felhasználó hitelesítésére és a megadott szintű hozzáférés elérésére használható.</span><span class="sxs-lookup"><span data-stu-id="35248-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="35248-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35248-113">EXAMPLES</span></span>

### <span data-ttu-id="35248-114">1. példa: Az engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncának le kérése</span><span class="sxs-lookup"><span data-stu-id="35248-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="35248-115">Ez a parancs a ContosoInternalHub értesítési központhoz rendelt szabály, a ListenRule engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="35248-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="35248-116">A parancsnak tartalmaznia kell a központi névteret és az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="35248-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="35248-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35248-117">PARAMETERS</span></span>

### <span data-ttu-id="35248-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="35248-118">-AuthorizationRule</span></span>
<span data-ttu-id="35248-119">A Megosztott hozzáférés-aláírás (SAS) hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35248-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="35248-120">Ezek a szabályok határozzák meg az értesítési központhoz való hozzáférés típusát.</span><span class="sxs-lookup"><span data-stu-id="35248-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="35248-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35248-121">-DefaultProfile</span></span>
<span data-ttu-id="35248-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="35248-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35248-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35248-123">-Namespace</span></span>
<span data-ttu-id="35248-124">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="35248-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="35248-125">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="35248-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="35248-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="35248-126">-NotificationHub</span></span>
<span data-ttu-id="35248-127">Azt az értesítési központot adja meg, amelyhez ez a parancsmag engedélyezési szabályt rendel.</span><span class="sxs-lookup"><span data-stu-id="35248-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="35248-128">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="35248-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="35248-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35248-129">-ResourceGroup</span></span>
<span data-ttu-id="35248-130">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="35248-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="35248-131">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="35248-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="35248-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35248-132">CommonParameters</span></span>
<span data-ttu-id="35248-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35248-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35248-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35248-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35248-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35248-135">INPUTS</span></span>

### <span data-ttu-id="35248-136">System.String</span><span class="sxs-lookup"><span data-stu-id="35248-136">System.String</span></span>

## <span data-ttu-id="35248-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35248-137">OUTPUTS</span></span>

### <span data-ttu-id="35248-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="35248-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="35248-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35248-139">NOTES</span></span>

## <span data-ttu-id="35248-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35248-140">RELATED LINKS</span></span>

[<span data-ttu-id="35248-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="35248-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


