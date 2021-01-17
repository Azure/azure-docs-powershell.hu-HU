---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336125"
---
# <span data-ttu-id="c9a2e-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c9a2e-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="c9a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a2e-103">Engedélyezési szabályokat állít be egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="c9a2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-104">SYNTAX</span></span>

### <span data-ttu-id="c9a2e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9a2e-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a2e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9a2e-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a2e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-107">DESCRIPTION</span></span>
<span data-ttu-id="c9a2e-108">A **Set-AzNotificationHubAuthorizationRule** parancsmag módosítja az értesítési központhoz rendelt MEGOSZTOTT hozzáférés-aláírás (SAS) engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="c9a2e-109">Az engedélyezési szabályok a különböző engedélyszintek alapján hivatkozások (URI-k) létrehozásával kezelik az értesítési központokhoz való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="c9a2e-110">A jogosultsági szintek az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="c9a2e-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="c9a2e-111">Hallgatás</span><span class="sxs-lookup"><span data-stu-id="c9a2e-111">Listen</span></span>
- <span data-ttu-id="c9a2e-112">Küldés</span><span class="sxs-lookup"><span data-stu-id="c9a2e-112">Send</span></span>
- <span data-ttu-id="c9a2e-113">Az ügyfelek kezelése a megfelelő engedélyszint alapján az alábbi URI-k egyikéhez irányítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="c9a2e-114">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz lesz irányítva.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="c9a2e-115">Ez a parancsmag kétféleképpen módosíthatja az értesítési központhoz rendelt engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="c9a2e-116">Az egyik esetben létrehozhatja a **SharedAccessAuthorizationRuleAttributes** objektum egy példányát, majd beállíthatja az objektumot a szabály birtokában található tulajdonságértékekkel.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="c9a2e-117">Az objektumot a .NET-keretrendszeren keresztül konfigurálhatja.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="c9a2e-118">Ezután a *SASRule* paraméter használatával átmásolhatja ezeket a tulajdonságértékeket a szabályba.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="c9a2e-119">Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a megfelelő konfigurációs értékeket, majd alkalmazza ezeket az értékeket az *InputFile paraméteren* keresztül.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="c9a2e-120">A JSON-fájl a következő szintaxishoz hasonló szintaxist használó szövegfájl: { "Név": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="c9a2e-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="c9a2e-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="c9a2e-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="c9a2e-122">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="c9a2e-122">"Rights": \[</span></span>  
        <span data-ttu-id="c9a2e-123">"Figyel",</span><span class="sxs-lookup"><span data-stu-id="c9a2e-123">"Listen",</span></span>  
        <span data-ttu-id="c9a2e-124">"Küldés"</span><span class="sxs-lookup"><span data-stu-id="c9a2e-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="c9a2e-125">} A New-AzNotificationHubAuthorizationRule-parancsmaggal együtt használva az előző JSON-minta módosít egy ContosoAuthorizationRule nevű engedélyezési szabályt, hogy a felhasználók figyelési és küldési jogosultságot adjanak a központnak.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="c9a2e-126">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9a2e-126">EXAMPLES</span></span>

### <span data-ttu-id="c9a2e-127">1. példa: Az értesítési központhoz rendelt engedélyezési szabály módosítása</span><span class="sxs-lookup"><span data-stu-id="c9a2e-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="c9a2e-128">Ez a parancs módosítja a ContosoExternalHub értesítési központhoz rendelt engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="c9a2e-129">Meg kell adnia a központ helyének névterét, valamint azt az erőforráscsoportot, amelyhez a központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="c9a2e-130">A módosított szabályra vonatkozó információk nem szerepelnek magában a parancsban.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="c9a2e-131">Ehelyett ez az információ megtalálható a bemeneti fájlban, C:\Configuration\AuthorizationRules.jsbe.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="c9a2e-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-132">PARAMETERS</span></span>

### <span data-ttu-id="c9a2e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a2e-133">-DefaultProfile</span></span>
<span data-ttu-id="c9a2e-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c9a2e-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9a2e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="c9a2e-135">-Force</span></span>
<span data-ttu-id="c9a2e-136">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-136">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9a2e-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c9a2e-137">-InputFile</span></span>
<span data-ttu-id="c9a2e-138">Az új szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="c9a2e-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c9a2e-139">-Namespace</span></span>
<span data-ttu-id="c9a2e-140">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c9a2e-141">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c9a2e-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c9a2e-142">-NotificationHub</span></span>
<span data-ttu-id="c9a2e-143">Megadja azt az értesítési központot, amelyhez ez a parancsmag engedélyezési szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="c9a2e-144">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, függetlenül attól, hogy ezeket az ügyfelek használják-e.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="c9a2e-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c9a2e-145">-ResourceGroup</span></span>
<span data-ttu-id="c9a2e-146">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="c9a2e-147">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c9a2e-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="c9a2e-148">-SASRule</span></span>
<span data-ttu-id="c9a2e-149">Megadja a **SharedAccessAuthorizationRuleAttributes** objektumot, amely a módosított engedélyezési szabályok konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="c9a2e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9a2e-150">-Confirm</span></span>
<span data-ttu-id="c9a2e-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a2e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a2e-152">-WhatIf</span></span>
<span data-ttu-id="c9a2e-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9a2e-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a2e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a2e-155">CommonParameters</span></span>
<span data-ttu-id="c9a2e-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a2e-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9a2e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a2e-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-158">INPUTS</span></span>

### <span data-ttu-id="c9a2e-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c9a2e-159">System.String</span></span>

## <span data-ttu-id="c9a2e-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9a2e-160">OUTPUTS</span></span>

### <span data-ttu-id="c9a2e-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c9a2e-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c9a2e-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9a2e-162">NOTES</span></span>

## <span data-ttu-id="c9a2e-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9a2e-163">RELATED LINKS</span></span>

[<span data-ttu-id="c9a2e-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c9a2e-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="c9a2e-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c9a2e-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="c9a2e-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c9a2e-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


