---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: 99cbaa3b6b1c6fc471c98abee1953049d06f904b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666001"
---
# <span data-ttu-id="adaad-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="adaad-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="adaad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adaad-102">SYNOPSIS</span></span>
<span data-ttu-id="adaad-103">Módosítja az integrációs fiók sémáját.</span><span class="sxs-lookup"><span data-stu-id="adaad-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="adaad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adaad-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adaad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adaad-105">DESCRIPTION</span></span>
<span data-ttu-id="adaad-106">A **set-AzIntegrationAccountSchema** parancsmag módosította az integrációs fiók sémáját.</span><span class="sxs-lookup"><span data-stu-id="adaad-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="adaad-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók sémáját jelképezi.</span><span class="sxs-lookup"><span data-stu-id="adaad-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="adaad-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a séma nevét.</span><span class="sxs-lookup"><span data-stu-id="adaad-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="adaad-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="adaad-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="adaad-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="adaad-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="adaad-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="adaad-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="adaad-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="adaad-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="adaad-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="adaad-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="adaad-114">Példák</span><span class="sxs-lookup"><span data-stu-id="adaad-114">EXAMPLES</span></span>

### <span data-ttu-id="adaad-115">Példa 1: az integrációs fiók sémájának módosítása</span><span class="sxs-lookup"><span data-stu-id="adaad-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="adaad-116">A parancs a IntegrationAccountSchema43 nevű integrációs fiók sémáját módosítja.</span><span class="sxs-lookup"><span data-stu-id="adaad-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="adaad-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adaad-117">PARAMETERS</span></span>

### <span data-ttu-id="adaad-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="adaad-118">-ContentType</span></span>
<span data-ttu-id="adaad-119">Az integrációs fiók sémájának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="adaad-120">Ez a parancsmag a térképes tartalomtípusként támogatja az Application/XML-t.</span><span class="sxs-lookup"><span data-stu-id="adaad-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaad-121">-DefaultProfile</span></span>
<span data-ttu-id="adaad-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="adaad-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adaad-123">-Force</span><span class="sxs-lookup"><span data-stu-id="adaad-123">-Force</span></span>
<span data-ttu-id="adaad-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="adaad-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adaad-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="adaad-125">-Metadata</span></span>
<span data-ttu-id="adaad-126">A séma metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-126">Specifies a metadata object for the schema.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="adaad-127">-Name</span></span>
<span data-ttu-id="adaad-128">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-128">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adaad-129">-ResourceGroupName</span></span>
<span data-ttu-id="adaad-130">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-130">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="adaad-131">-SchemaDefinition</span></span>
<span data-ttu-id="adaad-132">Az integrációs fiók sémájának meghatározási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-132">Specifies a definition object for integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="adaad-133">-SchemaFilePath</span></span>
<span data-ttu-id="adaad-134">Az integrációs fiók sémájának definíciójának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-134">Specifies the file path of a definition for the integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="adaad-135">-SchemaName</span></span>
<span data-ttu-id="adaad-136">Az integrációs fiók sémájának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-136">Specifies the name of the integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="adaad-137">-SchemaType</span></span>
<span data-ttu-id="adaad-138">Az integrációs fiók sémájának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaad-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="adaad-139">Ez a paraméter az XML típust támogatja.</span><span class="sxs-lookup"><span data-stu-id="adaad-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="adaad-140">-Confirm</span></span>
<span data-ttu-id="adaad-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="adaad-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adaad-142">-WhatIf</span></span>
<span data-ttu-id="adaad-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="adaad-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adaad-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adaad-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adaad-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaad-145">CommonParameters</span></span>
<span data-ttu-id="adaad-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adaad-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaad-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adaad-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaad-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adaad-148">INPUTS</span></span>

### <span data-ttu-id="adaad-149">System. String</span><span class="sxs-lookup"><span data-stu-id="adaad-149">System.String</span></span>

## <span data-ttu-id="adaad-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adaad-150">OUTPUTS</span></span>

### <span data-ttu-id="adaad-151">Microsoft. Azure. Management. Logic. models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="adaad-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="adaad-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adaad-152">NOTES</span></span>

## <span data-ttu-id="adaad-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adaad-153">RELATED LINKS</span></span>

[<span data-ttu-id="adaad-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="adaad-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="adaad-155">Új – AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="adaad-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="adaad-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="adaad-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


