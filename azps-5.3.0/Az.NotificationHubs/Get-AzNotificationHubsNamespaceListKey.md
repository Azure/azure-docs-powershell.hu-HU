---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479848"
---
# <span data-ttu-id="ea06e-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="ea06e-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="ea06e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea06e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea06e-103">Behozza az értesítési központ névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="ea06e-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="ea06e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea06e-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea06e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea06e-105">DESCRIPTION</span></span>
<span data-ttu-id="ea06e-106">A **Get-AzNotificationHubsNamespaceListKey** parancsmag egy értesítési központ névterhez rendelt Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ea06e-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="ea06e-107">Az engedélyezési szabályok az értesítési központ névteréhez való felhasználói jogokat kezelik.</span><span class="sxs-lookup"><span data-stu-id="ea06e-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="ea06e-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="ea06e-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="ea06e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea06e-109">EXAMPLES</span></span>

### <span data-ttu-id="ea06e-110">1. példa: Az engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncának le kérése</span><span class="sxs-lookup"><span data-stu-id="ea06e-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ea06e-111">Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ea06e-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="ea06e-112">A parancs futtatásakor meg kell lennie annak az erőforráscsoportnak a nevével, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ea06e-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="ea06e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea06e-113">PARAMETERS</span></span>

### <span data-ttu-id="ea06e-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea06e-114">-AuthorizationRule</span></span>
<span data-ttu-id="ea06e-115">Egy SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea06e-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="ea06e-116">Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel férnek hozzá az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="ea06e-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="ea06e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea06e-117">-DefaultProfile</span></span>
<span data-ttu-id="ea06e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ea06e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea06e-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea06e-119">-Namespace</span></span>
<span data-ttu-id="ea06e-120">Az a névtér, amely a parancsmag által lekért kapcsolati karakterláncokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ea06e-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ea06e-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea06e-121">-ResourceGroup</span></span>
<span data-ttu-id="ea06e-122">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ea06e-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="ea06e-123">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="ea06e-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ea06e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea06e-124">CommonParameters</span></span>
<span data-ttu-id="ea06e-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea06e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea06e-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea06e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea06e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea06e-127">INPUTS</span></span>

### <span data-ttu-id="ea06e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ea06e-128">System.String</span></span>

## <span data-ttu-id="ea06e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea06e-129">OUTPUTS</span></span>

### <span data-ttu-id="ea06e-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="ea06e-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="ea06e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea06e-131">NOTES</span></span>

## <span data-ttu-id="ea06e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea06e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ea06e-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ea06e-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ea06e-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea06e-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


