---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494774"
---
# <span data-ttu-id="16547-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="16547-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="16547-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16547-102">SYNOPSIS</span></span>
<span data-ttu-id="16547-103">Engedélyezési szabályokat állít be az értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="16547-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16547-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16547-104">SYNTAX</span></span>

### <span data-ttu-id="16547-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="16547-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16547-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="16547-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16547-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="16547-107">DESCRIPTION</span></span>
<span data-ttu-id="16547-108">A **set-AzureRmNotificationHubAuthorizationRules** parancsmag egy értesítési központhoz rendelt megosztott hozzáférés-aláírási (SAS) engedélyezési szabályt módosít.</span><span class="sxs-lookup"><span data-stu-id="16547-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="16547-109">Az engedélyezési szabályok a hozzáférést az értesítési hubokhoz az URI-k létrehozásával, különböző jogosultsági szintek alapján kezelik.</span><span class="sxs-lookup"><span data-stu-id="16547-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="16547-110">A jogosultsági szint az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="16547-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="16547-111">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="16547-111">Listen</span></span>
- <span data-ttu-id="16547-112">Küldése</span><span class="sxs-lookup"><span data-stu-id="16547-112">Send</span></span>
- <span data-ttu-id="16547-113">Kezelése</span><span class="sxs-lookup"><span data-stu-id="16547-113">Manage</span></span>

<span data-ttu-id="16547-114">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="16547-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="16547-115">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="16547-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="16547-116">Ez a parancsmag két módszert biztosít az értesítési központhoz rendelt engedélyezési szabályok módosítására.</span><span class="sxs-lookup"><span data-stu-id="16547-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="16547-117">Ehhez létre kell hoznia egy példányát a **SharedAccessAuthorizationRuleAttributes** objektumból, majd konfigurálnia kell az objektumot azokkal a tulajdonsági értékekkel, amelyeket a szabálynak meg szeretne jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="16547-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="16547-118">Az objektumot a .NET-keretrendszeren keresztül lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="16547-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="16547-119">Ezt követően a *SASRule* paraméterrel másolhatja az adott tulajdonság értékét a szabályba.</span><span class="sxs-lookup"><span data-stu-id="16547-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="16547-120">Azt is megteheti, hogy létrehoz egy JSON-fájlt (JavaScript-objektum jelölését), amely tartalmazza a megfelelő konfigurációs értékeket, majd ezeket az értékeket a *InputFile* paraméterrel alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="16547-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="16547-121">A JSON-fájl egy olyan szöveges fájl, amely az alábbihoz hasonló szintaxist használ:</span><span class="sxs-lookup"><span data-stu-id="16547-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="16547-122">{"Név": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="16547-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="16547-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="16547-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="16547-124">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="16547-124">"Rights": \[</span></span>  
        <span data-ttu-id="16547-125">"Figyelj",</span><span class="sxs-lookup"><span data-stu-id="16547-125">"Listen",</span></span>  
        <span data-ttu-id="16547-126">Küldése</span><span class="sxs-lookup"><span data-stu-id="16547-126">"Send"</span></span>  
    \]  
<span data-ttu-id="16547-127">}</span><span class="sxs-lookup"><span data-stu-id="16547-127">}</span></span>

<span data-ttu-id="16547-128">Ha az New-AzureRmNotificationHubAuthorizationRules parancsmaggal együtt használja, az előző JSON-minta módosítja a ContosoAuthorizationRule nevű engedélyezési szabályt, hogy a felhasználók hallgassanak és küldjenek jogokat a központnak.</span><span class="sxs-lookup"><span data-stu-id="16547-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="16547-129">Példák</span><span class="sxs-lookup"><span data-stu-id="16547-129">EXAMPLES</span></span>

### <span data-ttu-id="16547-130">Példa 1: az értesítési központhoz rendelt engedélyezési szabály módosítása</span><span class="sxs-lookup"><span data-stu-id="16547-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="16547-131">Ez a parancs módosítja a ContosoExternalHub nevű értesítési központhoz rendelt engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="16547-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="16547-132">Meg kell adnia azt a névteret, ahol a hub található, valamint a hub által kiosztott erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="16547-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="16547-133">A módosított szabályra vonatkozó információk nem szerepelnek a parancsban.</span><span class="sxs-lookup"><span data-stu-id="16547-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="16547-134">Ehelyett az információ megtalálható a bemeneti fájlban C:\Configuration\AuthorizationRules.jsbe elemre.</span><span class="sxs-lookup"><span data-stu-id="16547-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="16547-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16547-135">PARAMETERS</span></span>

### <span data-ttu-id="16547-136">-Force</span><span class="sxs-lookup"><span data-stu-id="16547-136">-Force</span></span>
<span data-ttu-id="16547-137">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16547-137">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16547-138">-InputFile</span><span class="sxs-lookup"><span data-stu-id="16547-138">-InputFile</span></span>
<span data-ttu-id="16547-139">Az új szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="16547-139">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="16547-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16547-140">-Namespace</span></span>
<span data-ttu-id="16547-141">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="16547-141">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="16547-142">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="16547-142">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="16547-143">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="16547-143">-NotificationHub</span></span>
<span data-ttu-id="16547-144">Annak az értesítési csomópontnak a megadása, amelyhez a parancsmag engedélyezési szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="16547-144">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="16547-145">Az értesítési hubok a leküldéses értesítéseket több ügyfélnek küldi el, függetlenül attól, hogy milyen ügyfelek használják őket.</span><span class="sxs-lookup"><span data-stu-id="16547-145">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="16547-146">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16547-146">-ResourceGroup</span></span>
<span data-ttu-id="16547-147">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="16547-147">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="16547-148">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="16547-148">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="16547-149">-SASRule</span><span class="sxs-lookup"><span data-stu-id="16547-149">-SASRule</span></span>
<span data-ttu-id="16547-150">Azt a **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg, amely a módosított engedélyezési szabályok konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="16547-150">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="16547-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16547-151">-Confirm</span></span>
<span data-ttu-id="16547-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16547-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16547-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16547-153">-WhatIf</span></span>
<span data-ttu-id="16547-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16547-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16547-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16547-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16547-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16547-156">-DefaultProfile</span></span>
<span data-ttu-id="16547-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16547-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16547-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16547-158">CommonParameters</span></span>
<span data-ttu-id="16547-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16547-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16547-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16547-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16547-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16547-161">INPUTS</span></span>

## <span data-ttu-id="16547-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16547-162">OUTPUTS</span></span>

### <span data-ttu-id="16547-163">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="16547-163">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="16547-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16547-164">NOTES</span></span>

## <span data-ttu-id="16547-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16547-165">RELATED LINKS</span></span>

[<span data-ttu-id="16547-166">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="16547-166">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="16547-167">Új – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="16547-167">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="16547-168">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="16547-168">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


