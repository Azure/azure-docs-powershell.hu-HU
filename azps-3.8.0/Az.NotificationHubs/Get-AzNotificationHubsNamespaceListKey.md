---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 90e617f35442470cef2d11c2de032679698ea167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846694"
---
# <span data-ttu-id="a0dd2-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="a0dd2-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="a0dd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a0dd2-103">Az értesítési hub névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="a0dd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0dd2-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0dd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a0dd2-106">A **Get-AzNotificationHubsNamespaceListKey** parancsmag a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncait számítja ki az értesítési hub névteréhez rendelve.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="a0dd2-107">Az engedélyezési szabályok a felhasználói jogokat az értesítési hub névteréhez kezelik.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="a0dd2-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="a0dd2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a0dd2-109">EXAMPLES</span></span>

### <span data-ttu-id="a0dd2-110">Példa 1: az elsődleges és másodlagos kapcsolati karakterláncok beszerzése egy engedélyezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="a0dd2-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="a0dd2-111">Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule nevű engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncait ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="a0dd2-112">A parancs futtatásakor tartalmaznia kell annak az erőforráscsoportnak a nevét, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="a0dd2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0dd2-113">PARAMETERS</span></span>

### <span data-ttu-id="a0dd2-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a0dd2-114">-AuthorizationRule</span></span>
<span data-ttu-id="a0dd2-115">A SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="a0dd2-116">Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="a0dd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0dd2-117">-DefaultProfile</span></span>
<span data-ttu-id="a0dd2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0dd2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0dd2-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a0dd2-119">-Namespace</span></span>
<span data-ttu-id="a0dd2-120">A parancsmag által kapott kapcsolati karakterláncokat tartalmazó névtér megadása.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0dd2-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0dd2-121">-ResourceGroup</span></span>
<span data-ttu-id="a0dd2-122">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="a0dd2-123">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a0dd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0dd2-124">CommonParameters</span></span>
<span data-ttu-id="a0dd2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0dd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0dd2-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0dd2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0dd2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0dd2-127">INPUTS</span></span>

### <span data-ttu-id="a0dd2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a0dd2-128">System.String</span></span>

## <span data-ttu-id="a0dd2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0dd2-129">OUTPUTS</span></span>

### <span data-ttu-id="a0dd2-130">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="a0dd2-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="a0dd2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0dd2-131">NOTES</span></span>

## <span data-ttu-id="a0dd2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0dd2-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0dd2-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a0dd2-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a0dd2-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0dd2-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


