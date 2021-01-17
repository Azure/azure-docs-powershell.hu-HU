---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467293"
---
# <span data-ttu-id="2e62b-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e62b-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="2e62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e62b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e62b-103">Engedélyezési szabályt hoz létre, és hozzárendeli azt egy értesítési központ névterhez.</span><span class="sxs-lookup"><span data-stu-id="2e62b-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="2e62b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e62b-104">SYNTAX</span></span>

### <span data-ttu-id="2e62b-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e62b-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e62b-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e62b-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e62b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e62b-107">DESCRIPTION</span></span>
<span data-ttu-id="2e62b-108">A **New-AzNotificationHubsNamespaceAuthorizationRule parancsmag** létrehoz egy SAS engedélyezési szabályt, és hozzárendeli egy értesítési központ névterhez.</span><span class="sxs-lookup"><span data-stu-id="2e62b-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="2e62b-109">Az engedélyezési szabályok kezelik a névtérhez és az adott névtérhez foglalt értesítési központok felhasználói jogait.</span><span class="sxs-lookup"><span data-stu-id="2e62b-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="2e62b-110">Ez a parancsmag két módszert biztosít új engedélyezési szabály létrehozására és névtérhez való hozzárendelésére.</span><span class="sxs-lookup"><span data-stu-id="2e62b-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="2e62b-111">Létrehozhatja a **SharedAccessAuthorizationRuleAttributes** objektum egy példányát, majd beállíthatja az objektumot a tulajdonságértékekkel, amelyekre az új szabálynak rendelkeznie kell.</span><span class="sxs-lookup"><span data-stu-id="2e62b-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="2e62b-112">Ezt a .NET-keretrendszer használatával lehet tenni.</span><span class="sxs-lookup"><span data-stu-id="2e62b-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="2e62b-113">Ezután az *SASRule* paraméter használatával átmásolhatja ezeket a tulajdonságértékeket az új szabályba.</span><span class="sxs-lookup"><span data-stu-id="2e62b-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="2e62b-114">Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a vonatkozó konfigurációs értékeket, majd az *InputFile* paraméter használatával alkalmazza ezeket az értékeket.</span><span class="sxs-lookup"><span data-stu-id="2e62b-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="2e62b-115">A JSON-fájl olyan szövegfájl, amely a következő szintaxist használja: {</span><span class="sxs-lookup"><span data-stu-id="2e62b-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="2e62b-116">"Név": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="2e62b-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="2e62b-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="2e62b-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="2e62b-118">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="2e62b-118">"Rights": \[</span></span>  
        <span data-ttu-id="2e62b-119">"Figyel",</span><span class="sxs-lookup"><span data-stu-id="2e62b-119">"Listen",</span></span>  
        <span data-ttu-id="2e62b-120">"Küldés"</span><span class="sxs-lookup"><span data-stu-id="2e62b-120">"Send"</span></span>  
    \]  
<span data-ttu-id="2e62b-121">} A **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmaggal együtt használva az előző JSON-minta létrehoz egy ContosoAuthorizationRule nevű engedélyezési szabályt, amely a felhasználó figyelási és küldési jogosultságát biztosítja a névtérhez.</span><span class="sxs-lookup"><span data-stu-id="2e62b-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="2e62b-122">A hitelesítéshez használt *PrimaryKey* a következő Windows PowerShell-paranccsal generálható véletlenszerűen: \[ Convert \] ::ToBase64String((1.32 |% { \[ bájt/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="2e62b-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="2e62b-123">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e62b-123">EXAMPLES</span></span>

### <span data-ttu-id="2e62b-124">1. példa: Engedélyezési szabály létrehozása és hozzárendelése egy névtérhez</span><span class="sxs-lookup"><span data-stu-id="2e62b-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="2e62b-125">Ez a parancs létrehoz egy engedélyezési szabályt, és hozzárendeli azt a ContosoNamespace névtérhez.</span><span class="sxs-lookup"><span data-stu-id="2e62b-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="2e62b-126">A szabály létrehozásakor meg kell adnia a megfelelő névteret és azt az erőforráscsoportot, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2e62b-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="2e62b-127">Magára a szabályra vonatkozó információt azonban nem kell megadnia: a szabályinformációk a beviteli fájlból fognak C:\Configuration\NamespaceAuthorizationRules.jsbe.</span><span class="sxs-lookup"><span data-stu-id="2e62b-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="2e62b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e62b-128">PARAMETERS</span></span>

### <span data-ttu-id="2e62b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e62b-129">-DefaultProfile</span></span>
<span data-ttu-id="2e62b-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e62b-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e62b-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2e62b-131">-InputFile</span></span>
<span data-ttu-id="2e62b-132">Az új engedélyezési szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e62b-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e62b-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e62b-133">-Namespace</span></span>
<span data-ttu-id="2e62b-134">Azt a névteret adja meg, amelyhez az engedélyezési szabályokat hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="2e62b-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="2e62b-135">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="2e62b-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="2e62b-136">Az új szabályokat hozzá kell rendelni egy meglévő névtérhez.</span><span class="sxs-lookup"><span data-stu-id="2e62b-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="2e62b-137">A **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmag nem tud új névteret létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2e62b-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="2e62b-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2e62b-138">-ResourceGroup</span></span>
<span data-ttu-id="2e62b-139">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="2e62b-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="2e62b-140">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="2e62b-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="2e62b-141">Meglévő erőforráscsoportot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="2e62b-141">You must use an existing resource group.</span></span>
<span data-ttu-id="2e62b-142">Ez a parancsmag nem tud új erőforráscsoportot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2e62b-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="2e62b-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="2e62b-143">-SASRule</span></span>
<span data-ttu-id="2e62b-144">Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e62b-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e62b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e62b-145">-Confirm</span></span>
<span data-ttu-id="2e62b-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e62b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e62b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e62b-147">-WhatIf</span></span>
<span data-ttu-id="2e62b-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e62b-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e62b-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e62b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e62b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e62b-150">CommonParameters</span></span>
<span data-ttu-id="2e62b-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e62b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e62b-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e62b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e62b-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e62b-153">INPUTS</span></span>

### <span data-ttu-id="2e62b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2e62b-154">System.String</span></span>

## <span data-ttu-id="2e62b-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e62b-155">OUTPUTS</span></span>

### <span data-ttu-id="2e62b-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2e62b-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2e62b-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e62b-157">NOTES</span></span>

## <span data-ttu-id="2e62b-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e62b-158">RELATED LINKS</span></span>

[<span data-ttu-id="2e62b-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e62b-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="2e62b-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e62b-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="2e62b-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e62b-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


