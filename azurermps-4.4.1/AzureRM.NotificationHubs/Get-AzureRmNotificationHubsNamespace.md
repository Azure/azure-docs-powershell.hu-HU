---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494787"
---
# <span data-ttu-id="61dec-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61dec-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="61dec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61dec-102">SYNOPSIS</span></span>
<span data-ttu-id="61dec-103">Információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="61dec-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61dec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61dec-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61dec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61dec-105">DESCRIPTION</span></span>
<span data-ttu-id="61dec-106">**A Get-AzureRmNotificationHubsNamespace** parancsmag információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="61dec-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="61dec-107">Ez a parancsmag lehetőséget nyújt arra, hogy az összes névtérre vonatkozóan információt kapjanak, és hogy a megadott erőforráscsoporthoz rendelt névterekre vonatkozóan milyen információkra van szükség. vagy egy adott névtérről szóló információk visszaadására.</span><span class="sxs-lookup"><span data-stu-id="61dec-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="61dec-108">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="61dec-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="61dec-109">Legalább egy értesítési hub-névtérnek kell lennie: minden értesítési hubot egy névtérhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="61dec-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="61dec-110">Egyetlen névtérben több hub jelenhet meg, ami azt jelenti, hogy csak egy névtérre van szüksége a szervezetében.</span><span class="sxs-lookup"><span data-stu-id="61dec-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="61dec-111">Több névtér is használható azonban a hubok jobb rendszerezéséhez, vagy ha konkrét személyekre engedélyt szeretne adni a hubok kijelölt részhalmazának kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="61dec-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="61dec-112">A **Get-AzureRmNotificationHubsNamespace** parancsmag a névtérre vonatkozó alapvető információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="61dec-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="61dec-113">Ha a névtérhez társított engedélyezési szabályokról szeretne információt kapni, használja a Get-AzureRmNotificationHubsNamespaceAuthorizationRulest.</span><span class="sxs-lookup"><span data-stu-id="61dec-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="61dec-114">Példák</span><span class="sxs-lookup"><span data-stu-id="61dec-114">EXAMPLES</span></span>

### <span data-ttu-id="61dec-115">1. példa: információk kérése az összes értesítési hub-névtérről</span><span class="sxs-lookup"><span data-stu-id="61dec-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="61dec-116">Ez a parancs információt ad az összes értesítési hub-névtérről.</span><span class="sxs-lookup"><span data-stu-id="61dec-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="61dec-117">2. példa: információk beszerzése egyetlen értesítési központi névtérről</span><span class="sxs-lookup"><span data-stu-id="61dec-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="61dec-118">Ez a parancs egyetlen értesítési hub-névtérről kap információt: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="61dec-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="61dec-119">3. példa: információk kérése egy adott névtérhez rendelt minden értesítési hubhoz</span><span class="sxs-lookup"><span data-stu-id="61dec-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="61dec-120">Ez a parancs információt kap az erőforráscsoport ContosoNotificationsGroup társított összes értesítési hub-névtérről.</span><span class="sxs-lookup"><span data-stu-id="61dec-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="61dec-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61dec-121">PARAMETERS</span></span>

### <span data-ttu-id="61dec-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="61dec-122">-Namespace</span></span>
<span data-ttu-id="61dec-123">A névtér egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61dec-123">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="61dec-124">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="61dec-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="61dec-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61dec-125">-ResourceGroup</span></span>
<span data-ttu-id="61dec-126">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="61dec-126">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="61dec-127">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="61dec-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="61dec-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dec-128">-DefaultProfile</span></span>
<span data-ttu-id="61dec-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61dec-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61dec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dec-130">CommonParameters</span></span>
<span data-ttu-id="61dec-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61dec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dec-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61dec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dec-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61dec-133">INPUTS</span></span>

## <span data-ttu-id="61dec-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61dec-134">OUTPUTS</span></span>

### <span data-ttu-id="61dec-135">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. models. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="61dec-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="61dec-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61dec-136">NOTES</span></span>

## <span data-ttu-id="61dec-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61dec-137">RELATED LINKS</span></span>

[<span data-ttu-id="61dec-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="61dec-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="61dec-139">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61dec-139">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="61dec-140">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61dec-140">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="61dec-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61dec-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


