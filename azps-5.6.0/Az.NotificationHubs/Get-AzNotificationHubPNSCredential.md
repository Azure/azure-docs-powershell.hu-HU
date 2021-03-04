---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 44da06fa8237880be154100d05eeee60cd7db7b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918273"
---
# <span data-ttu-id="d9415-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="d9415-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="d9415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9415-102">SYNOPSIS</span></span>
<span data-ttu-id="d9415-103">Egy értesítési központ PNS-hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9415-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="d9415-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9415-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9415-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9415-105">DESCRIPTION</span></span>
<span data-ttu-id="d9415-106">A **Get-AzNotificationHubPNSCredential** parancsmag megkapja az értesítési központ platformértesítési szolgáltatásának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="d9415-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="d9415-107">Minden értesítési központ egyetlen PNS-hitelesítő adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="d9415-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="d9415-108">Ezeket a hitelesítő adatokat az egyes leküldéses értesítési szolgáltatásokra alkalmazza a rendszer, de nem kizárólagosan; az iOS leküldéses értesítési szolgáltatás, az Android leküldéses értesítéseket szolgáltató és a Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="d9415-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="d9415-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9415-109">EXAMPLES</span></span>

### <span data-ttu-id="d9415-110">1. példa: A PNS-hez szükséges hitelesítő adatok lekérte egy adott értesítési központhoz</span><span class="sxs-lookup"><span data-stu-id="d9415-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="d9415-111">Ez a parancs a ContosoInternalHub nevű értesítési központ PNS-hitelesítő adatait kapja meg, amely a ContosoNotificationsGroup nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="d9415-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="d9415-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9415-112">PARAMETERS</span></span>

### <span data-ttu-id="d9415-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9415-113">-DefaultProfile</span></span>
<span data-ttu-id="d9415-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9415-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9415-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d9415-115">-Namespace</span></span>
<span data-ttu-id="d9415-116">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d9415-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d9415-117">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="d9415-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d9415-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9415-118">-NotificationHub</span></span>
<span data-ttu-id="d9415-119">Azt az értesítési központot adja meg, amelyhez a PNS-hitelesítő adatok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="d9415-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="d9415-120">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="d9415-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="d9415-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9415-121">-ResourceGroup</span></span>
<span data-ttu-id="d9415-122">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d9415-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="d9415-123">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="d9415-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d9415-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9415-124">CommonParameters</span></span>
<span data-ttu-id="d9415-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9415-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9415-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9415-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9415-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9415-127">INPUTS</span></span>

### <span data-ttu-id="d9415-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d9415-128">System.String</span></span>

## <span data-ttu-id="d9415-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9415-129">OUTPUTS</span></span>

### <span data-ttu-id="d9415-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d9415-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="d9415-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9415-131">NOTES</span></span>

## <span data-ttu-id="d9415-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9415-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9415-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9415-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


