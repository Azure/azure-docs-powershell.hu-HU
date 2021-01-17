---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336210"
---
# <span data-ttu-id="dfbec-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dfbec-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="dfbec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfbec-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbec-103">Engedélyezési szabályt hoz létre, és hozzárendeli a szabályt egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="dfbec-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="dfbec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dfbec-104">SYNTAX</span></span>

### <span data-ttu-id="dfbec-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfbec-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbec-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfbec-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfbec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dfbec-107">DESCRIPTION</span></span>
<span data-ttu-id="dfbec-108">A **New-AzNotificationHubAuthorizationRule** parancsmag létrehoz egy értesítési központ Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="dfbec-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="dfbec-109">Az engedélyezési szabályok az értesítési központokhoz való hozzáférés kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="dfbec-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="dfbec-110">Ezt a különböző jogosultsági szinteken alapuló hivatkozások URI-k létrehozásával lehet tenni.</span><span class="sxs-lookup"><span data-stu-id="dfbec-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="dfbec-111">Az ügyfél a megfelelő jogosultsági szint alapján az alábbi URI-k egyikére irányítja az URI-ket.</span><span class="sxs-lookup"><span data-stu-id="dfbec-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="dfbec-112">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz lesz irányítva.</span><span class="sxs-lookup"><span data-stu-id="dfbec-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="dfbec-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dfbec-113">EXAMPLES</span></span>

### <span data-ttu-id="dfbec-114">1. példa: Értesítési központ engedélyezési szabályának létrehozása</span><span class="sxs-lookup"><span data-stu-id="dfbec-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="dfbec-115">Ez a parancs létrehoz egy új engedélyezési szabályt, és hozzárendeli azt a ContosoInternalHub nevű értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="dfbec-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="dfbec-116">Ez a központ a ContosoNamespace névterében található, és a ContosoNotificationsGroup erőforráscsoporthoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="dfbec-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="dfbec-117">Vegye figyelembe, hogy a szabály összes konfigurációs adata, beleértve a szabály nevét is, a bemeneti fájlból fog C:\Configuration\ExternalAccessRule.jsbe.</span><span class="sxs-lookup"><span data-stu-id="dfbec-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="dfbec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfbec-118">PARAMETERS</span></span>

### <span data-ttu-id="dfbec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbec-119">-DefaultProfile</span></span>
<span data-ttu-id="dfbec-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dfbec-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfbec-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="dfbec-121">-InputFile</span></span>
<span data-ttu-id="dfbec-122">A parancsmag által létrehozott engedélyezési szabály bemeneti fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfbec-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dfbec-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dfbec-123">-Namespace</span></span>
<span data-ttu-id="dfbec-124">Megadja azt a névteret, amelyhez az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="dfbec-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="dfbec-125">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="dfbec-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="dfbec-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="dfbec-126">-NotificationHub</span></span>
<span data-ttu-id="dfbec-127">Azt az értesítési központot adja meg, amelyhez az engedélyezési szabályokat hozzárendeli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="dfbec-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="dfbec-128">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="dfbec-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="dfbec-129">Ne feledje, hogy meg kell adnia egy meglévő értesítési központ nevét.</span><span class="sxs-lookup"><span data-stu-id="dfbec-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="dfbec-130">A **New-AzNotificationHubAuthorizationRule** parancsmag nem tud új értesítési központokat létrehozni.</span><span class="sxs-lookup"><span data-stu-id="dfbec-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="dfbec-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dfbec-131">-ResourceGroup</span></span>
<span data-ttu-id="dfbec-132">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="dfbec-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="dfbec-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="dfbec-133">-SASRule</span></span>
<span data-ttu-id="dfbec-134">Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfbec-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="dfbec-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfbec-135">-Confirm</span></span>
<span data-ttu-id="dfbec-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dfbec-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbec-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbec-137">-WhatIf</span></span>
<span data-ttu-id="dfbec-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dfbec-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfbec-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfbec-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbec-140">CommonParameters</span></span>
<span data-ttu-id="dfbec-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbec-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbec-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbec-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfbec-143">INPUTS</span></span>

### <span data-ttu-id="dfbec-144">System.String</span><span class="sxs-lookup"><span data-stu-id="dfbec-144">System.String</span></span>

## <span data-ttu-id="dfbec-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfbec-145">OUTPUTS</span></span>

### <span data-ttu-id="dfbec-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dfbec-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="dfbec-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dfbec-147">NOTES</span></span>

## <span data-ttu-id="dfbec-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfbec-148">RELATED LINKS</span></span>

[<span data-ttu-id="dfbec-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dfbec-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="dfbec-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dfbec-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="dfbec-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dfbec-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


