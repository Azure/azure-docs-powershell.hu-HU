---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501455"
---
# <span data-ttu-id="ae591-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ae591-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="ae591-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae591-102">SYNOPSIS</span></span>
<span data-ttu-id="ae591-103">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési hub-névtérhez.</span><span class="sxs-lookup"><span data-stu-id="ae591-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae591-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae591-104">SYNTAX</span></span>

### <span data-ttu-id="ae591-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae591-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae591-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae591-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae591-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae591-107">DESCRIPTION</span></span>
<span data-ttu-id="ae591-108">A **New-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmag létrehoz egy megosztott hozzáférés-aláírási (SA) engedélyezési szabályt, és hozzárendeli az értesítési hub névteréhez.</span><span class="sxs-lookup"><span data-stu-id="ae591-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="ae591-109">Az engedélyezési szabályok a névtérhez és az adott névtérhez tartozó értesítési hubokhoz való felhasználói jogokat kezelik.</span><span class="sxs-lookup"><span data-stu-id="ae591-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="ae591-110">Ez a parancsmag két lehetőséget kínál új engedélyezési szabály létrehozására és névtérhez rendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="ae591-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="ae591-111">Létrehozhat egy példányt a **SharedAccessAuthorizationRuleAttributes** objektumból, majd beállíthatja az objektum azon tulajdonsági értékeit, amelyeket az új szabálynak meg kell jelenítenie.</span><span class="sxs-lookup"><span data-stu-id="ae591-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="ae591-112">Ez a funkció a .NET Framework segítségével végezhető el.</span><span class="sxs-lookup"><span data-stu-id="ae591-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="ae591-113">A *SASRule* paraméterrel átmásolhatja ezeket a tulajdonságértékeket az új szabályba.</span><span class="sxs-lookup"><span data-stu-id="ae591-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="ae591-114">Azt is megteheti, hogy a megfelelő konfigurációs értékeket tartalmazó JSON (JavaScript-objektum jelölése) fájlt hoz létre, majd a *InputFile* paraméterrel alkalmazza ezeket az értékeket.</span><span class="sxs-lookup"><span data-stu-id="ae591-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="ae591-115">A JSON-fájl egy olyan szöveges fájl, amely az alábbihoz hasonló szintaxist használ:</span><span class="sxs-lookup"><span data-stu-id="ae591-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="ae591-116">{</span><span class="sxs-lookup"><span data-stu-id="ae591-116">{</span></span>  
    <span data-ttu-id="ae591-117">"Név": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="ae591-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="ae591-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="ae591-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="ae591-119">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="ae591-119">"Rights": \[</span></span>  
        <span data-ttu-id="ae591-120">"Figyelj",</span><span class="sxs-lookup"><span data-stu-id="ae591-120">"Listen",</span></span>  
        <span data-ttu-id="ae591-121">Küldése</span><span class="sxs-lookup"><span data-stu-id="ae591-121">"Send"</span></span>  
    \]  
<span data-ttu-id="ae591-122">}</span><span class="sxs-lookup"><span data-stu-id="ae591-122">}</span></span>

<span data-ttu-id="ae591-123">Ha a **New-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmaggal együtt használja, az előző JSON-minta létrehoz egy ContosoAuthorizationRule nevű engedélyezési szabályt, amely lehetővé teszi, hogy a felhasználók meghallgassák és elküldjék a névteret.</span><span class="sxs-lookup"><span data-stu-id="ae591-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="ae591-124">A hitelesítéshez használt *PrimaryKey* véletlenszerűen, a következő Windows PowerShell-parancs segítségével hozhatók létre:</span><span class="sxs-lookup"><span data-stu-id="ae591-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="ae591-125">\[Convert \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-Random-min. 0 – maximum 255)}))</span><span class="sxs-lookup"><span data-stu-id="ae591-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="ae591-126">Példák</span><span class="sxs-lookup"><span data-stu-id="ae591-126">EXAMPLES</span></span>

### <span data-ttu-id="ae591-127">Példa 1: engedélyezési szabály létrehozása és hozzárendelése egy névtérhez</span><span class="sxs-lookup"><span data-stu-id="ae591-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="ae591-128">A parancs létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt a névtér ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="ae591-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="ae591-129">A szabály létrehozásakor meg kell adnia a megfelelő névteret és azt az erőforráscsoport-csoportot, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ae591-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="ae591-130">Nem kell azonban a szabályra vonatkozó információkat megadni: a szabály adatait a program a bemeneti fájlból C:\Configuration\NamespaceAuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="ae591-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="ae591-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae591-131">PARAMETERS</span></span>

### <span data-ttu-id="ae591-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae591-132">-DefaultProfile</span></span>
<span data-ttu-id="ae591-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae591-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae591-134">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ae591-134">-InputFile</span></span>
<span data-ttu-id="ae591-135">Az új engedélyezési szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae591-135">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae591-136">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ae591-136">-Namespace</span></span>
<span data-ttu-id="ae591-137">Azt a névteret adja meg, amelyre az engedélyezési szabályokat hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="ae591-137">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="ae591-138">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="ae591-138">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="ae591-139">Az új szabályokat egy meglévő névtérhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="ae591-139">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="ae591-140">A **New-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmag nem tud új névteret létrehozni.</span><span class="sxs-lookup"><span data-stu-id="ae591-140">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="ae591-141">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae591-141">-ResourceGroup</span></span>
<span data-ttu-id="ae591-142">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="ae591-142">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="ae591-143">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="ae591-143">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="ae591-144">Egy meglévő erőforráscsoportot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="ae591-144">You must use an existing resource group.</span></span>
<span data-ttu-id="ae591-145">Ez a parancsmag nem tud új erőforráscsoportot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="ae591-145">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="ae591-146">-SASRule</span><span class="sxs-lookup"><span data-stu-id="ae591-146">-SASRule</span></span>
<span data-ttu-id="ae591-147">Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae591-147">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae591-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae591-148">-Confirm</span></span>
<span data-ttu-id="ae591-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae591-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae591-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae591-150">-WhatIf</span></span>
<span data-ttu-id="ae591-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae591-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae591-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae591-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae591-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae591-153">CommonParameters</span></span>
<span data-ttu-id="ae591-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae591-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae591-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae591-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae591-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae591-156">INPUTS</span></span>

### <span data-ttu-id="ae591-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="ae591-157">None</span></span>
<span data-ttu-id="ae591-158">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ae591-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae591-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae591-159">OUTPUTS</span></span>

### <span data-ttu-id="ae591-160">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ae591-160">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ae591-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae591-161">NOTES</span></span>

## <span data-ttu-id="ae591-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae591-162">RELATED LINKS</span></span>

[<span data-ttu-id="ae591-163">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ae591-163">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="ae591-164">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ae591-164">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="ae591-165">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ae591-165">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


