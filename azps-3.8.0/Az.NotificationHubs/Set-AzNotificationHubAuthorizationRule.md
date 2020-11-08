---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012767"
---
# <span data-ttu-id="84e75-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="84e75-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="84e75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84e75-102">SYNOPSIS</span></span>
<span data-ttu-id="84e75-103">Engedélyezési szabályokat állít be az értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="84e75-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="84e75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84e75-104">SYNTAX</span></span>

### <span data-ttu-id="84e75-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e75-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e75-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e75-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e75-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="84e75-107">DESCRIPTION</span></span>
<span data-ttu-id="84e75-108">A **set-AzNotificationHubAuthorizationRule** parancsmag egy értesítési központhoz rendelt megosztott hozzáférés-aláírási (SAS) engedélyezési szabályt módosít.</span><span class="sxs-lookup"><span data-stu-id="84e75-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="84e75-109">Az engedélyezési szabályok a hozzáférést az értesítési hubokhoz az URI-k létrehozásával, különböző jogosultsági szintek alapján kezelik.</span><span class="sxs-lookup"><span data-stu-id="84e75-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="84e75-110">A jogosultsági szint az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="84e75-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="84e75-111">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="84e75-111">Listen</span></span>
- <span data-ttu-id="84e75-112">Küldése</span><span class="sxs-lookup"><span data-stu-id="84e75-112">Send</span></span>
- <span data-ttu-id="84e75-113">Az ügyfelek kezelése a megfelelő jogosultsági szint alapján a fenti URI-k egyikéhez van irányítva.</span><span class="sxs-lookup"><span data-stu-id="84e75-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="84e75-114">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="84e75-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="84e75-115">Ez a parancsmag két módszert biztosít az értesítési központhoz rendelt engedélyezési szabályok módosítására.</span><span class="sxs-lookup"><span data-stu-id="84e75-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="84e75-116">Ehhez létre kell hoznia egy példányát a **SharedAccessAuthorizationRuleAttributes** objektumból, majd konfigurálnia kell az objektumot azokkal a tulajdonsági értékekkel, amelyeket a szabálynak meg szeretne jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="84e75-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="84e75-117">Az objektumot a .NET-keretrendszeren keresztül lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="84e75-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="84e75-118">Ezt követően a *SASRule* paraméterrel másolhatja az adott tulajdonság értékét a szabályba.</span><span class="sxs-lookup"><span data-stu-id="84e75-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="84e75-119">Azt is megteheti, hogy létrehoz egy JSON-fájlt (JavaScript-objektum jelölését), amely tartalmazza a megfelelő konfigurációs értékeket, majd ezeket az értékeket a *InputFile* paraméterrel alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="84e75-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="84e75-120">A JSON-fájl a következőhöz hasonló szintaxist használó szövegfájl: {"név": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="84e75-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="84e75-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="84e75-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="84e75-122">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="84e75-122">"Rights": \[</span></span>  
        <span data-ttu-id="84e75-123">"Figyelj",</span><span class="sxs-lookup"><span data-stu-id="84e75-123">"Listen",</span></span>  
        <span data-ttu-id="84e75-124">Küldése</span><span class="sxs-lookup"><span data-stu-id="84e75-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="84e75-125">} Ha az New-AzNotificationHubAuthorizationRule parancsmaggal együtt használja, az előző JSON-minta módosítja a ContosoAuthorizationRule nevű engedélyezési szabályt annak érdekében, hogy a felhasználók meghallgassák és elküldjék a központot.</span><span class="sxs-lookup"><span data-stu-id="84e75-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="84e75-126">Példák</span><span class="sxs-lookup"><span data-stu-id="84e75-126">EXAMPLES</span></span>

### <span data-ttu-id="84e75-127">Példa 1: az értesítési központhoz rendelt engedélyezési szabály módosítása</span><span class="sxs-lookup"><span data-stu-id="84e75-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="84e75-128">Ez a parancs módosítja a ContosoExternalHub nevű értesítési központhoz rendelt engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="84e75-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="84e75-129">Meg kell adnia azt a névteret, ahol a hub található, valamint a hub által kiosztott erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="84e75-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="84e75-130">A módosított szabályra vonatkozó információk nem szerepelnek a parancsban.</span><span class="sxs-lookup"><span data-stu-id="84e75-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="84e75-131">Ehelyett az információ megtalálható a bemeneti fájlban C:\Configuration\AuthorizationRules.jsbe elemre.</span><span class="sxs-lookup"><span data-stu-id="84e75-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="84e75-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84e75-132">PARAMETERS</span></span>

### <span data-ttu-id="84e75-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e75-133">-DefaultProfile</span></span>
<span data-ttu-id="84e75-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="84e75-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84e75-135">-Force</span><span class="sxs-lookup"><span data-stu-id="84e75-135">-Force</span></span>
<span data-ttu-id="84e75-136">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84e75-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="84e75-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="84e75-137">-InputFile</span></span>
<span data-ttu-id="84e75-138">Az új szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84e75-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="84e75-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84e75-139">-Namespace</span></span>
<span data-ttu-id="84e75-140">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="84e75-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="84e75-141">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="84e75-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="84e75-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="84e75-142">-NotificationHub</span></span>
<span data-ttu-id="84e75-143">Annak az értesítési csomópontnak a megadása, amelyhez a parancsmag engedélyezési szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="84e75-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="84e75-144">Az értesítési hubok a leküldéses értesítéseket több ügyfélnek küldi el, függetlenül attól, hogy milyen ügyfelek használják őket.</span><span class="sxs-lookup"><span data-stu-id="84e75-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="84e75-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="84e75-145">-ResourceGroup</span></span>
<span data-ttu-id="84e75-146">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="84e75-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="84e75-147">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="84e75-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="84e75-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="84e75-148">-SASRule</span></span>
<span data-ttu-id="84e75-149">Azt a **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg, amely a módosított engedélyezési szabályok konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="84e75-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="84e75-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="84e75-150">-Confirm</span></span>
<span data-ttu-id="84e75-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="84e75-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e75-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e75-152">-WhatIf</span></span>
<span data-ttu-id="84e75-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="84e75-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84e75-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84e75-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e75-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e75-155">CommonParameters</span></span>
<span data-ttu-id="84e75-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84e75-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e75-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e75-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e75-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84e75-158">INPUTS</span></span>

### <span data-ttu-id="84e75-159">System. String</span><span class="sxs-lookup"><span data-stu-id="84e75-159">System.String</span></span>

## <span data-ttu-id="84e75-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84e75-160">OUTPUTS</span></span>

### <span data-ttu-id="84e75-161">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="84e75-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="84e75-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84e75-162">NOTES</span></span>

## <span data-ttu-id="84e75-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84e75-163">RELATED LINKS</span></span>

[<span data-ttu-id="84e75-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="84e75-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="84e75-165">Új – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="84e75-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="84e75-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="84e75-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


