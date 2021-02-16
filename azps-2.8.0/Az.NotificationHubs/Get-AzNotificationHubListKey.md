---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 7ce6c3c08c1794e2bed794186203a5c6c0d1fdea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413761"
---
# <span data-ttu-id="dd41e-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="dd41e-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="dd41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd41e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd41e-103">Lekérte az értesítési központ engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="dd41e-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="dd41e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd41e-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd41e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd41e-105">DESCRIPTION</span></span>
<span data-ttu-id="dd41e-106">A **Get-AzNotificationHubListKey** parancsmag egy értesítési központ Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="dd41e-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="dd41e-107">Az engedélyezési szabályok kezelik a központ felhasználói jogait.</span><span class="sxs-lookup"><span data-stu-id="dd41e-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="dd41e-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="dd41e-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="dd41e-109">Az alábbi kapcsolati karakterláncok (URI-k) az alábbi műveleteket hajtják végre:</span><span class="sxs-lookup"><span data-stu-id="dd41e-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="dd41e-110">Mutasson a felhasználóknak egy erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="dd41e-110">Point users to a resource.</span></span>
- <span data-ttu-id="dd41e-111">Lekérdezésparamétereket tartalmazó jogkivonatot is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="dd41e-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="dd41e-112">A paraméterek egyike, az aláírás a felhasználó hitelesítésére és a megadott szintű hozzáférés biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="dd41e-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="dd41e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd41e-113">EXAMPLES</span></span>

### <span data-ttu-id="dd41e-114">1. példa: Az engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncának le kérése</span><span class="sxs-lookup"><span data-stu-id="dd41e-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="dd41e-115">Ez a parancs a ContosoInternalHub értesítési központhoz rendelt szabály, a ListenRule engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd41e-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="dd41e-116">A parancsnak tartalmaznia kell a központi névteret és az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="dd41e-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="dd41e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd41e-117">PARAMETERS</span></span>

### <span data-ttu-id="dd41e-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dd41e-118">-AuthorizationRule</span></span>
<span data-ttu-id="dd41e-119">A Megosztott hozzáférés-aláírás (SAS) hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd41e-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="dd41e-120">Ezek a szabályok határozzák meg az értesítési központhoz való hozzáférés típusát.</span><span class="sxs-lookup"><span data-stu-id="dd41e-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="dd41e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd41e-121">-DefaultProfile</span></span>
<span data-ttu-id="dd41e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dd41e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd41e-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd41e-123">-Namespace</span></span>
<span data-ttu-id="dd41e-124">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="dd41e-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="dd41e-125">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="dd41e-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="dd41e-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="dd41e-126">-NotificationHub</span></span>
<span data-ttu-id="dd41e-127">Azt az értesítési központot adja meg, amelyhez ez a parancsmag engedélyezési szabályt rendel.</span><span class="sxs-lookup"><span data-stu-id="dd41e-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="dd41e-128">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, függetlenül attól, hogy milyen platformot használnak az adott ügyfél által használt platformon.</span><span class="sxs-lookup"><span data-stu-id="dd41e-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="dd41e-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dd41e-129">-ResourceGroup</span></span>
<span data-ttu-id="dd41e-130">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="dd41e-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="dd41e-131">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="dd41e-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="dd41e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd41e-132">CommonParameters</span></span>
<span data-ttu-id="dd41e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd41e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd41e-134">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd41e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd41e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd41e-135">INPUTS</span></span>

### <span data-ttu-id="dd41e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dd41e-136">System.String</span></span>

## <span data-ttu-id="dd41e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd41e-137">OUTPUTS</span></span>

### <span data-ttu-id="dd41e-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="dd41e-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="dd41e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd41e-139">NOTES</span></span>

## <span data-ttu-id="dd41e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd41e-140">RELATED LINKS</span></span>



