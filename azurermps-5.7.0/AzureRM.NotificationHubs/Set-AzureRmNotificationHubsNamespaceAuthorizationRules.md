---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ed94e34f754298e89bf1f18d5264f11c2c9c308c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505423"
---
# <span data-ttu-id="628e4-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="628e4-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="628e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="628e4-102">SYNOPSIS</span></span>
<span data-ttu-id="628e4-103">Az értesítési hub névterének engedélyezési szabályait állítja be.</span><span class="sxs-lookup"><span data-stu-id="628e4-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="628e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="628e4-104">SYNTAX</span></span>

### <span data-ttu-id="628e4-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="628e4-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="628e4-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="628e4-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="628e4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="628e4-107">DESCRIPTION</span></span>
<span data-ttu-id="628e4-108">A **set-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmag egy értesítési hub-névtérhez rendelt megosztott hozzáférés-aláírási engedélyezési szabályt módosít.</span><span class="sxs-lookup"><span data-stu-id="628e4-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="628e4-109">Az engedélyezési szabályok a névtérhez és az adott névtérben lévő értesítési hubokhoz való felhasználói jogokat kezelik.</span><span class="sxs-lookup"><span data-stu-id="628e4-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="628e4-110">Ez a parancsmag két módszert biztosít a névtérhez rendelt engedélyezési szabályok módosítására.</span><span class="sxs-lookup"><span data-stu-id="628e4-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="628e4-111">Ehhez létre kell hoznia egy példányát a **SharedAccessAuthorizationRuleAttributes** objektumból, majd konfigurálnia kell az objektumot azokkal a tulajdonsági értékekkel, amelyeket a szabálynak meg szeretne jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="628e4-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="628e4-112">Ezt a .NET-keretrendszer segítségével végezheti el.</span><span class="sxs-lookup"><span data-stu-id="628e4-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="628e4-113">Ezután a *SASRule* paraméterrel átmásolhatja ezeket a tulajdonságokat a szabályba.</span><span class="sxs-lookup"><span data-stu-id="628e4-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="628e4-114">Azt is megteheti, hogy létrehoz egy JSON-fájlt (JavaScript-objektum jelölését), amely tartalmazza a megfelelő konfigurációs értékeket, majd ezeket az értékeket a *InputFile* paraméterrel alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="628e4-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="628e4-115">A JSON-fájl egy olyan szöveges fájl, amely az alábbihoz hasonló szintaxist használ:</span><span class="sxs-lookup"><span data-stu-id="628e4-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="628e4-116">{</span><span class="sxs-lookup"><span data-stu-id="628e4-116">{</span></span>  
    <span data-ttu-id="628e4-117">"Név": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="628e4-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="628e4-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="628e4-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="628e4-119">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="628e4-119">"Rights": \[</span></span>  
        <span data-ttu-id="628e4-120">"Figyelj",</span><span class="sxs-lookup"><span data-stu-id="628e4-120">"Listen",</span></span>  
        <span data-ttu-id="628e4-121">Küldése</span><span class="sxs-lookup"><span data-stu-id="628e4-121">"Send"</span></span>  
    \]  
<span data-ttu-id="628e4-122">}</span><span class="sxs-lookup"><span data-stu-id="628e4-122">}</span></span>

<span data-ttu-id="628e4-123">Ha a **set-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmaggal együtt használja, az előző JSON-minta módosítja a ContosoAuthorizationRule nevű engedélyezési szabályt, hogy a felhasználók meghallgassák és elküldjék a névteret.</span><span class="sxs-lookup"><span data-stu-id="628e4-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="628e4-124">Példák</span><span class="sxs-lookup"><span data-stu-id="628e4-124">EXAMPLES</span></span>

### <span data-ttu-id="628e4-125">Példa 1: névtérhez rendelt engedélyezési szabály módosítása</span><span class="sxs-lookup"><span data-stu-id="628e4-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="628e4-126">Ez a parancs módosítja a ContosoNamespace nevű névtérhez rendelt engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="628e4-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="628e4-127">Meg kell adnia a névtérhez rendelt erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="628e4-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="628e4-128">Az engedélyezési szabályról szóló információk nem szerepelnek a parancsban.</span><span class="sxs-lookup"><span data-stu-id="628e4-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="628e4-129">Ehelyett ezt az információt a bemeneti fájlból C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="628e4-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="628e4-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="628e4-130">PARAMETERS</span></span>

### <span data-ttu-id="628e4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628e4-131">-DefaultProfile</span></span>
<span data-ttu-id="628e4-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="628e4-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="628e4-133">-Force</span><span class="sxs-lookup"><span data-stu-id="628e4-133">-Force</span></span>
<span data-ttu-id="628e4-134">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="628e4-134">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628e4-135">-InputFile</span><span class="sxs-lookup"><span data-stu-id="628e4-135">-InputFile</span></span>
<span data-ttu-id="628e4-136">Az új szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="628e4-136">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="628e4-137">-Namespace</span><span class="sxs-lookup"><span data-stu-id="628e4-137">-Namespace</span></span>
<span data-ttu-id="628e4-138">Azt a névteret adja meg, amely a parancsmag által módosított engedélyezési szabályokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="628e4-138">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="628e4-139">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="628e4-139">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="628e4-140">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="628e4-140">-ResourceGroup</span></span>
<span data-ttu-id="628e4-141">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="628e4-141">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="628e4-142">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="628e4-142">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="628e4-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="628e4-143">-SASRule</span></span>
<span data-ttu-id="628e4-144">Azt a **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg, amely a parancsmag által módosított engedélyezési szabályok konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="628e4-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="628e4-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="628e4-145">-Confirm</span></span>
<span data-ttu-id="628e4-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="628e4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="628e4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="628e4-147">-WhatIf</span></span>
<span data-ttu-id="628e4-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="628e4-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="628e4-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="628e4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="628e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628e4-150">CommonParameters</span></span>
<span data-ttu-id="628e4-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="628e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628e4-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="628e4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628e4-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="628e4-153">INPUTS</span></span>

### <span data-ttu-id="628e4-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="628e4-154">None</span></span>
<span data-ttu-id="628e4-155">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="628e4-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="628e4-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="628e4-156">OUTPUTS</span></span>

### <span data-ttu-id="628e4-157">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="628e4-157">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="628e4-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="628e4-158">NOTES</span></span>

## <span data-ttu-id="628e4-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="628e4-159">RELATED LINKS</span></span>

[<span data-ttu-id="628e4-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="628e4-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="628e4-161">Új – AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="628e4-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="628e4-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="628e4-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


