---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 0c834f8ee24090fa0da11f6c01fb0ddad3251756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500795"
---
# <span data-ttu-id="c153f-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="c153f-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="c153f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c153f-102">SYNOPSIS</span></span>
<span data-ttu-id="c153f-103">Az értesítési hub névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c153f-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c153f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c153f-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c153f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c153f-105">DESCRIPTION</span></span>
<span data-ttu-id="c153f-106">A **Get-AzureRmNotificationHubsNamespaceListKeys** parancsmag a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncait számítja ki az értesítési hub névteréhez rendelve.</span><span class="sxs-lookup"><span data-stu-id="c153f-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="c153f-107">Az engedélyezési szabályok a felhasználói jogokat az értesítési hub névteréhez kezelik.</span><span class="sxs-lookup"><span data-stu-id="c153f-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="c153f-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="c153f-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="c153f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c153f-109">EXAMPLES</span></span>

### <span data-ttu-id="c153f-110">Példa 1: az elsődleges és másodlagos kapcsolati karakterláncok beszerzése egy engedélyezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="c153f-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c153f-111">Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule nevű engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncait ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c153f-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="c153f-112">A parancs futtatásakor tartalmaznia kell annak az erőforráscsoportnak a nevét, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c153f-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="c153f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c153f-113">PARAMETERS</span></span>

### <span data-ttu-id="c153f-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c153f-114">-AuthorizationRule</span></span>
<span data-ttu-id="c153f-115">A SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c153f-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="c153f-116">Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="c153f-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="c153f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c153f-117">-Namespace</span></span>
<span data-ttu-id="c153f-118">A parancsmag által kapott kapcsolati karakterláncokat tartalmazó névtér megadása.</span><span class="sxs-lookup"><span data-stu-id="c153f-118">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c153f-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c153f-119">-ResourceGroup</span></span>
<span data-ttu-id="c153f-120">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="c153f-120">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="c153f-121">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="c153f-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c153f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c153f-122">-DefaultProfile</span></span>
<span data-ttu-id="c153f-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c153f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c153f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c153f-124">CommonParameters</span></span>
<span data-ttu-id="c153f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c153f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c153f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c153f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c153f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c153f-127">INPUTS</span></span>

## <span data-ttu-id="c153f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c153f-128">OUTPUTS</span></span>

### <span data-ttu-id="c153f-129">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c153f-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c153f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c153f-130">NOTES</span></span>

## <span data-ttu-id="c153f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c153f-131">RELATED LINKS</span></span>

[<span data-ttu-id="c153f-132">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c153f-132">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="c153f-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c153f-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


