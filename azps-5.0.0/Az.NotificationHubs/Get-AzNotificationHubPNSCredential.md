---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186056"
---
# <span data-ttu-id="8cfc9-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="8cfc9-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="8cfc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfc9-103">Beolvassa az értesítési központ PNS hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="8cfc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cfc9-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cfc9-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfc9-106">A **Get-AzNotificationHubPNSCredential** parancsmag az értesítési központ platform értesítési szolgáltatásának (PNS) hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="8cfc9-107">Minden egyes értesítési hub egyetlen PNS hitelesítő adatkészletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="8cfc9-108">Ezek a hitelesítő adatok az egyes leküldéses értesítési szolgáltatásokra érvényesek, például a nem korlátozottak; az iOS Leküldéses értesítési szolgáltatás, az Android leküldéses értesítő szolgáltatás és a Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="8cfc9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8cfc9-109">EXAMPLES</span></span>

### <span data-ttu-id="8cfc9-110">Példa 1: PNS hitelesítő adatok beszerzése egy adott értesítési központhoz</span><span class="sxs-lookup"><span data-stu-id="8cfc9-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8cfc9-111">Ez a parancs a ContosoNotificationsGroup nevű erőforráscsoport ContosoInternalHub tartozó PNS hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="8cfc9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cfc9-112">PARAMETERS</span></span>

### <span data-ttu-id="8cfc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfc9-113">-DefaultProfile</span></span>
<span data-ttu-id="8cfc9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8cfc9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cfc9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8cfc9-115">-Namespace</span></span>
<span data-ttu-id="8cfc9-116">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8cfc9-117">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8cfc9-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8cfc9-118">-NotificationHub</span></span>
<span data-ttu-id="8cfc9-119">Annak az értesítési csomópontnak a megadása, amelyhez a PNS hitelesítő adatai hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="8cfc9-120">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8cfc9-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cfc9-121">-ResourceGroup</span></span>
<span data-ttu-id="8cfc9-122">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8cfc9-123">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="8cfc9-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8cfc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfc9-124">CommonParameters</span></span>
<span data-ttu-id="8cfc9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cfc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfc9-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfc9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfc9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cfc9-127">INPUTS</span></span>

### <span data-ttu-id="8cfc9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8cfc9-128">System.String</span></span>

## <span data-ttu-id="8cfc9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cfc9-129">OUTPUTS</span></span>

### <span data-ttu-id="8cfc9-130">Microsoft. Azure. Command. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8cfc9-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="8cfc9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cfc9-131">NOTES</span></span>

## <span data-ttu-id="8cfc9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cfc9-132">RELATED LINKS</span></span>

[<span data-ttu-id="8cfc9-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8cfc9-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


