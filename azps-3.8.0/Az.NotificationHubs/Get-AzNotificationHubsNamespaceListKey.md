---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 5244602a6b6266ebabf02bbb927facda93e61d8b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403799"
---
# <span data-ttu-id="803fc-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="803fc-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="803fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="803fc-102">SYNOPSIS</span></span>
<span data-ttu-id="803fc-103">Egy értesítési központ névtér-engedélyezési szabályával társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="803fc-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="803fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="803fc-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="803fc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="803fc-105">DESCRIPTION</span></span>
<span data-ttu-id="803fc-106">A **Get-AzNotificationHubsNamespaceListKey** parancsmag egy értesítési központ névterhez rendelt Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="803fc-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="803fc-107">Az engedélyezési szabályok az értesítési központ névteréhez való felhasználói jogokat kezelik.</span><span class="sxs-lookup"><span data-stu-id="803fc-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="803fc-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="803fc-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="803fc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="803fc-109">EXAMPLES</span></span>

### <span data-ttu-id="803fc-110">1. példa: Az engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncának le kérése</span><span class="sxs-lookup"><span data-stu-id="803fc-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="803fc-111">Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="803fc-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="803fc-112">A parancs futtatásakor meg kell lennie annak az erőforráscsoportnak a nevével, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="803fc-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="803fc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="803fc-113">PARAMETERS</span></span>

### <span data-ttu-id="803fc-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="803fc-114">-AuthorizationRule</span></span>
<span data-ttu-id="803fc-115">Egy SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="803fc-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="803fc-116">Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel férnek hozzá az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="803fc-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="803fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803fc-117">-DefaultProfile</span></span>
<span data-ttu-id="803fc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="803fc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="803fc-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="803fc-119">-Namespace</span></span>
<span data-ttu-id="803fc-120">Az a névtér, amely a parancsmag által lekért kapcsolati karakterláncokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="803fc-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="803fc-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="803fc-121">-ResourceGroup</span></span>
<span data-ttu-id="803fc-122">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="803fc-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="803fc-123">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="803fc-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="803fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803fc-124">CommonParameters</span></span>
<span data-ttu-id="803fc-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="803fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803fc-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="803fc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803fc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="803fc-127">INPUTS</span></span>

### <span data-ttu-id="803fc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="803fc-128">System.String</span></span>

## <span data-ttu-id="803fc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="803fc-129">OUTPUTS</span></span>

### <span data-ttu-id="803fc-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="803fc-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="803fc-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="803fc-131">NOTES</span></span>

## <span data-ttu-id="803fc-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="803fc-132">RELATED LINKS</span></span>

[<span data-ttu-id="803fc-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="803fc-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



