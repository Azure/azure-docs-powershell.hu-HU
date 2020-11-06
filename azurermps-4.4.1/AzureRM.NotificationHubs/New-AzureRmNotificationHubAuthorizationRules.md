---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497028"
---
# <span data-ttu-id="f6acb-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6acb-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="f6acb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6acb-102">SYNOPSIS</span></span>
<span data-ttu-id="f6acb-103">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="f6acb-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6acb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6acb-104">SYNTAX</span></span>

### <span data-ttu-id="f6acb-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6acb-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6acb-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6acb-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6acb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6acb-107">DESCRIPTION</span></span>
<span data-ttu-id="f6acb-108">A **New-AzureRmNotificationHubAuthorizationRules** parancsmag létrehoz egy értesítési hubot a megosztott hozzáférés-aláírási (SAS) engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="f6acb-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="f6acb-109">Az engedélyezési szabályok az értesítési hubok elérésének kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="f6acb-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="f6acb-110">Ezt úgy teheti meg, hogy a különböző jogosultsági szintek alapján URI-ként hozza létre a hivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="f6acb-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f6acb-111">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="f6acb-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f6acb-112">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="f6acb-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="f6acb-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f6acb-113">EXAMPLES</span></span>

### <span data-ttu-id="f6acb-114">Példa 1: értesítési hub engedélyezési szabályának létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6acb-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="f6acb-115">A parancs új engedélyezési szabályt hoz létre, és hozzárendeli a ContosoInternalHub nevű értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="f6acb-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="f6acb-116">Ez a hub a ContosoNamespace névtérben található, és a ContosoNotificationsGroup erőforrás csoportjába van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f6acb-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="f6acb-117">Figyelje meg, hogy a szabály összes konfigurációs adatát (a szabály nevét is) a program a bemeneti fájlból C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="f6acb-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="f6acb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6acb-118">PARAMETERS</span></span>

### <span data-ttu-id="f6acb-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f6acb-119">-InputFile</span></span>
<span data-ttu-id="f6acb-120">A parancsmag által létrehozott engedélyezési szabály bemeneti fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6acb-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6acb-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6acb-121">-Namespace</span></span>
<span data-ttu-id="f6acb-122">Azt a névteret adja meg, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="f6acb-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f6acb-123">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="f6acb-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f6acb-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6acb-124">-NotificationHub</span></span>
<span data-ttu-id="f6acb-125">Itt adhatja meg azt az értesítési központot, amelyre az engedélyezési szabályok hozzá lesznek rendelve.</span><span class="sxs-lookup"><span data-stu-id="f6acb-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="f6acb-126">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="f6acb-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="f6acb-127">Fontos tudni, hogy meg kell adnia egy meglévő értesítési központ nevét.</span><span class="sxs-lookup"><span data-stu-id="f6acb-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="f6acb-128">A **New-AzureRmNotificationHubAuthorizationRules** parancsmag nem tud új értesítési hubokat létrehozni.</span><span class="sxs-lookup"><span data-stu-id="f6acb-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="f6acb-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f6acb-129">-ResourceGroup</span></span>
<span data-ttu-id="f6acb-130">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f6acb-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="f6acb-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="f6acb-131">-SASRule</span></span>
<span data-ttu-id="f6acb-132">Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6acb-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6acb-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6acb-133">-Confirm</span></span>
<span data-ttu-id="f6acb-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6acb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6acb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6acb-135">-WhatIf</span></span>
<span data-ttu-id="f6acb-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6acb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6acb-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6acb-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6acb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6acb-138">-DefaultProfile</span></span>
<span data-ttu-id="f6acb-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6acb-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6acb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6acb-140">CommonParameters</span></span>
<span data-ttu-id="f6acb-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6acb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6acb-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6acb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6acb-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6acb-143">INPUTS</span></span>

## <span data-ttu-id="f6acb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6acb-144">OUTPUTS</span></span>

### <span data-ttu-id="f6acb-145">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f6acb-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f6acb-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6acb-146">NOTES</span></span>

## <span data-ttu-id="f6acb-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6acb-147">RELATED LINKS</span></span>

[<span data-ttu-id="f6acb-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6acb-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="f6acb-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6acb-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="f6acb-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6acb-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


