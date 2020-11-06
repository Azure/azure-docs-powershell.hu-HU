---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespacelistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 2fb9eeb3b5d6bcc3a2183bc652b74caa370e4d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496359"
---
# <span data-ttu-id="f8fe1-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="f8fe1-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="f8fe1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fe1-103">Az értesítési hub névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8fe1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8fe1-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8fe1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8fe1-105">DESCRIPTION</span></span>
<span data-ttu-id="f8fe1-106">A **Get-AzureRmNotificationHubsNamespaceListKeys** parancsmag a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncait számítja ki az értesítési hub névteréhez rendelve.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="f8fe1-107">Az engedélyezési szabályok a felhasználói jogokat az értesítési hub névteréhez kezelik.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="f8fe1-108">Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="f8fe1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f8fe1-109">EXAMPLES</span></span>

### <span data-ttu-id="f8fe1-110">Példa 1: az elsődleges és másodlagos kapcsolati karakterláncok beszerzése egy engedélyezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="f8fe1-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f8fe1-111">Ez a parancs a ContosoNamespace névtérhez rendelt ListenRule nevű engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncait ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="f8fe1-112">A parancs futtatásakor tartalmaznia kell annak az erőforráscsoportnak a nevét, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="f8fe1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8fe1-113">PARAMETERS</span></span>

### <span data-ttu-id="f8fe1-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8fe1-114">-AuthorizationRule</span></span>
<span data-ttu-id="f8fe1-115">A SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="f8fe1-116">Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-116">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8fe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fe1-117">-DefaultProfile</span></span>
<span data-ttu-id="f8fe1-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f8fe1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fe1-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8fe1-119">-Namespace</span></span>
<span data-ttu-id="f8fe1-120">A parancsmag által kapott kapcsolati karakterláncokat tartalmazó névtér megadása.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8fe1-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8fe1-121">-ResourceGroup</span></span>
<span data-ttu-id="f8fe1-122">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-122">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="f8fe1-123">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8fe1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fe1-124">CommonParameters</span></span>
<span data-ttu-id="f8fe1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8fe1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fe1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8fe1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fe1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8fe1-127">INPUTS</span></span>

### <span data-ttu-id="f8fe1-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="f8fe1-128">None</span></span>
<span data-ttu-id="f8fe1-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f8fe1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8fe1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8fe1-130">OUTPUTS</span></span>

### <span data-ttu-id="f8fe1-131">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="f8fe1-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="f8fe1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8fe1-132">NOTES</span></span>

## <span data-ttu-id="f8fe1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8fe1-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8fe1-134">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f8fe1-134">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f8fe1-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f8fe1-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


