---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206438"
---
# <span data-ttu-id="97e0b-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="97e0b-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="97e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="97e0b-103">Információkat kap egy értesítési központ névterről.</span><span class="sxs-lookup"><span data-stu-id="97e0b-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="97e0b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97e0b-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97e0b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="97e0b-106">**A Get-AzNotificationHubsNamespace** parancsmag információt kap az értesítési központ névtereiről.</span><span class="sxs-lookup"><span data-stu-id="97e0b-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="97e0b-107">Ez a parancsmag lehetőséget nyújt arra, hogy információt kap az összes névtérről, valamint egy adott erőforráscsoporthoz rendelt névterek adatairól; vagy adott névtérről ad vissza információkat.</span><span class="sxs-lookup"><span data-stu-id="97e0b-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="97e0b-108">A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.</span><span class="sxs-lookup"><span data-stu-id="97e0b-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="97e0b-109">Legalább egy értesítési központ névterének meg kell lennie osztva: az összes értesítési központot hozzá kell rendelni egy névtérhez.</span><span class="sxs-lookup"><span data-stu-id="97e0b-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="97e0b-110">Egy névtér több központi központban is elterjedhet, ami azt jelenti, hogy a szervezetben lehet, hogy csak egy névterre van szüksége.</span><span class="sxs-lookup"><span data-stu-id="97e0b-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="97e0b-111">Több névteret is adhat azonban, hogy jobban rendszerezze a központokat, vagy hogy egyes személyeknek engedélyt adjon a központok kijelölt alcsoportja kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="97e0b-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="97e0b-112">A **Get-AzNotificationHubsNamespace** parancsmag alapvető információkat ad vissza a névtérről.</span><span class="sxs-lookup"><span data-stu-id="97e0b-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="97e0b-113">A névtérhez társított engedélyezési szabályokról a Get-AzNotificationHubsNamespaceAuthorizationRules használatával tud információt kapni.</span><span class="sxs-lookup"><span data-stu-id="97e0b-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="97e0b-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97e0b-114">EXAMPLES</span></span>

### <span data-ttu-id="97e0b-115">1. példa: Információk lekérte az értesítési központ összes névterét</span><span class="sxs-lookup"><span data-stu-id="97e0b-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="97e0b-116">Ez a parancs az értesítési központ összes névterének adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="97e0b-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="97e0b-117">2. példa: Információ lekérte egy értesítési központ névterét</span><span class="sxs-lookup"><span data-stu-id="97e0b-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="97e0b-118">Ez a parancs információt kap egyetlen értesítési központ névterére: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="97e0b-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="97e0b-119">3. példa: Információ az adott névtérhez rendelt összes értesítési központról</span><span class="sxs-lookup"><span data-stu-id="97e0b-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="97e0b-120">Ez a parancs információkat kap a ContosoNotificationsGroup erőforráscsoporthoz rendelt összes értesítési központ névterével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="97e0b-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="97e0b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97e0b-121">PARAMETERS</span></span>

### <span data-ttu-id="97e0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e0b-122">-DefaultProfile</span></span>
<span data-ttu-id="97e0b-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97e0b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97e0b-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="97e0b-124">-Namespace</span></span>
<span data-ttu-id="97e0b-125">A névtér egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97e0b-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="97e0b-126">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="97e0b-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="97e0b-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97e0b-127">-ResourceGroup</span></span>
<span data-ttu-id="97e0b-128">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="97e0b-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="97e0b-129">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="97e0b-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="97e0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e0b-130">CommonParameters</span></span>
<span data-ttu-id="97e0b-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e0b-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e0b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e0b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97e0b-133">INPUTS</span></span>

### <span data-ttu-id="97e0b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="97e0b-134">System.String</span></span>

## <span data-ttu-id="97e0b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e0b-135">OUTPUTS</span></span>

### <span data-ttu-id="97e0b-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="97e0b-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="97e0b-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97e0b-137">NOTES</span></span>

## <span data-ttu-id="97e0b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97e0b-138">RELATED LINKS</span></span>

[<span data-ttu-id="97e0b-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="97e0b-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="97e0b-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="97e0b-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="97e0b-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="97e0b-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="97e0b-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="97e0b-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


