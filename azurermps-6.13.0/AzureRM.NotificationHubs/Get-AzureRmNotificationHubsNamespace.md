---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b4603566b793cbded7e593c9e4a23c3788c140de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504315"
---
# <span data-ttu-id="1a95a-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1a95a-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="1a95a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a95a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a95a-103">Információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="1a95a-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a95a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a95a-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a95a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a95a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a95a-106">**A Get-AzureRmNotificationHubsNamespace** parancsmag információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="1a95a-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="1a95a-107">Ez a parancsmag lehetőséget nyújt arra, hogy az összes névtérre vonatkozóan információt kapjanak, és hogy a megadott erőforráscsoporthoz rendelt névterekre vonatkozóan milyen információkra van szükség. vagy egy adott névtérről szóló információk visszaadására.</span><span class="sxs-lookup"><span data-stu-id="1a95a-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="1a95a-108">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="1a95a-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="1a95a-109">Legalább egy értesítési hub-névtérnek kell lennie: minden értesítési hubot egy névtérhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="1a95a-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="1a95a-110">Egyetlen névtérben több hub jelenhet meg, ami azt jelenti, hogy csak egy névtérre van szüksége a szervezetében.</span><span class="sxs-lookup"><span data-stu-id="1a95a-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="1a95a-111">Több névtér is használható azonban a hubok jobb rendszerezéséhez, vagy ha konkrét személyekre engedélyt szeretne adni a hubok kijelölt részhalmazának kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="1a95a-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="1a95a-112">A **Get-AzureRmNotificationHubsNamespace** parancsmag a névtérre vonatkozó alapvető információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1a95a-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="1a95a-113">Ha a névtérhez társított engedélyezési szabályokról szeretne információt kapni, használja a Get-AzureRmNotificationHubsNamespaceAuthorizationRulest.</span><span class="sxs-lookup"><span data-stu-id="1a95a-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="1a95a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1a95a-114">EXAMPLES</span></span>

### <span data-ttu-id="1a95a-115">1. példa: információk kérése az összes értesítési hub-névtérről</span><span class="sxs-lookup"><span data-stu-id="1a95a-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="1a95a-116">Ez a parancs információt ad az összes értesítési hub-névtérről.</span><span class="sxs-lookup"><span data-stu-id="1a95a-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="1a95a-117">2. példa: információk beszerzése egyetlen értesítési központi névtérről</span><span class="sxs-lookup"><span data-stu-id="1a95a-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="1a95a-118">Ez a parancs egyetlen értesítési hub-névtérről kap információt: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="1a95a-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="1a95a-119">3. példa: információk kérése egy adott névtérhez rendelt minden értesítési hubhoz</span><span class="sxs-lookup"><span data-stu-id="1a95a-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1a95a-120">Ez a parancs információt kap az erőforráscsoport ContosoNotificationsGroup társított összes értesítési hub-névtérről.</span><span class="sxs-lookup"><span data-stu-id="1a95a-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="1a95a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a95a-121">PARAMETERS</span></span>

### <span data-ttu-id="1a95a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a95a-122">-DefaultProfile</span></span>
<span data-ttu-id="1a95a-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1a95a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a95a-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1a95a-124">-Namespace</span></span>
<span data-ttu-id="1a95a-125">A névtér egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a95a-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="1a95a-126">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="1a95a-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a95a-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a95a-127">-ResourceGroup</span></span>
<span data-ttu-id="1a95a-128">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="1a95a-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1a95a-129">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="1a95a-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a95a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a95a-130">CommonParameters</span></span>
<span data-ttu-id="1a95a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a95a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a95a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a95a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a95a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a95a-133">INPUTS</span></span>

### <span data-ttu-id="1a95a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1a95a-134">System.String</span></span>

## <span data-ttu-id="1a95a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a95a-135">OUTPUTS</span></span>

### <span data-ttu-id="1a95a-136">Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1a95a-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="1a95a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a95a-137">NOTES</span></span>

## <span data-ttu-id="1a95a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a95a-138">RELATED LINKS</span></span>

[<span data-ttu-id="1a95a-139">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1a95a-139">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="1a95a-140">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1a95a-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="1a95a-141">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1a95a-141">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="1a95a-142">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1a95a-142">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


