---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 436ed6aaa720074be2014d9c736ab0636a09869f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669903"
---
# <span data-ttu-id="5f6a6-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f6a6-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="5f6a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f6a6-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6a6-103">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="5f6a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f6a6-104">SYNTAX</span></span>

### <span data-ttu-id="5f6a6-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f6a6-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f6a6-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f6a6-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f6a6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f6a6-107">DESCRIPTION</span></span>
<span data-ttu-id="5f6a6-108">A **New-AzNotificationHubAuthorizationRule** parancsmag létrehoz egy értesítési hubot a megosztott hozzáférés-aláírási (SAS) engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="5f6a6-109">Az engedélyezési szabályok az értesítési hubok elérésének kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="5f6a6-110">Ezt úgy teheti meg, hogy a különböző jogosultsági szintek alapján URI-ként hozza létre a hivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="5f6a6-111">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="5f6a6-112">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="5f6a6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5f6a6-113">EXAMPLES</span></span>

### <span data-ttu-id="5f6a6-114">Példa 1: értesítési hub engedélyezési szabályának létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f6a6-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="5f6a6-115">A parancs új engedélyezési szabályt hoz létre, és hozzárendeli a ContosoInternalHub nevű értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="5f6a6-116">Ez a hub a ContosoNamespace névtérben található, és a ContosoNotificationsGroup erőforrás csoportjába van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="5f6a6-117">Figyelje meg, hogy a szabály összes konfigurációs adatát (a szabály nevét is) a program a bemeneti fájlból C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="5f6a6-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f6a6-118">PARAMETERS</span></span>

### <span data-ttu-id="5f6a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6a6-119">-DefaultProfile</span></span>
<span data-ttu-id="5f6a6-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5f6a6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f6a6-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5f6a6-121">-InputFile</span></span>
<span data-ttu-id="5f6a6-122">A parancsmag által létrehozott engedélyezési szabály bemeneti fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5f6a6-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f6a6-123">-Namespace</span></span>
<span data-ttu-id="5f6a6-124">Azt a névteret adja meg, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="5f6a6-125">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5f6a6-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="5f6a6-126">-NotificationHub</span></span>
<span data-ttu-id="5f6a6-127">Itt adhatja meg azt az értesítési központot, amelyre az engedélyezési szabályok hozzá lesznek rendelve.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="5f6a6-128">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="5f6a6-129">Fontos tudni, hogy meg kell adnia egy meglévő értesítési központ nevét.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="5f6a6-130">A **New-AzNotificationHubAuthorizationRule** parancsmag nem tud új értesítési hubokat létrehozni.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="5f6a6-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f6a6-131">-ResourceGroup</span></span>
<span data-ttu-id="5f6a6-132">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="5f6a6-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="5f6a6-133">-SASRule</span></span>
<span data-ttu-id="5f6a6-134">Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="5f6a6-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f6a6-135">-Confirm</span></span>
<span data-ttu-id="5f6a6-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6a6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6a6-137">-WhatIf</span></span>
<span data-ttu-id="5f6a6-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f6a6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6a6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6a6-140">CommonParameters</span></span>
<span data-ttu-id="5f6a6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f6a6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6a6-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6a6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6a6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f6a6-143">INPUTS</span></span>

### <span data-ttu-id="5f6a6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5f6a6-144">System.String</span></span>

## <span data-ttu-id="5f6a6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f6a6-145">OUTPUTS</span></span>

### <span data-ttu-id="5f6a6-146">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5f6a6-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5f6a6-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f6a6-147">NOTES</span></span>

## <span data-ttu-id="5f6a6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f6a6-148">RELATED LINKS</span></span>

[<span data-ttu-id="5f6a6-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f6a6-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5f6a6-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f6a6-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5f6a6-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f6a6-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


