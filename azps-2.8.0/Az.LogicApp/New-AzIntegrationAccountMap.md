---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: e483d2f88f12655283c94d8c42e9926e4dd6cddb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666050"
---
# <span data-ttu-id="5bbd7-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bbd7-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="5bbd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbd7-103">Az integrációs fiók megfeleltetését hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-103">Creates an integration account map.</span></span>

## <span data-ttu-id="5bbd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bbd7-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bbd7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bbd7-105">DESCRIPTION</span></span>
<span data-ttu-id="5bbd7-106">A **New-AzIntegrationAccountMap** parancsmag létrehoz egy integrációs fiók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="5bbd7-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók megfeleltetését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="5bbd7-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét, a megfeleltetés nevét és a Térkép definícióját.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="5bbd7-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="5bbd7-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5bbd7-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5bbd7-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5bbd7-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5bbd7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="5bbd7-114">EXAMPLES</span></span>

### <span data-ttu-id="5bbd7-115">1. példa: az integrációs fiók megfeleltetésének létrehozása</span><span class="sxs-lookup"><span data-stu-id="5bbd7-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="5bbd7-116">Ez a parancs létrehozza az integrációs fiók megfeleltetését a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="5bbd7-117">A parancs a $MapContent változóban egy korábbi parancs által tárolt megfeleltetési definíciót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="5bbd7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bbd7-118">PARAMETERS</span></span>

### <span data-ttu-id="5bbd7-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5bbd7-119">-ContentType</span></span>
<span data-ttu-id="5bbd7-120">Az integrációs fiók megfeleltetésének tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="5bbd7-121">Ez a parancsmag a térképes tartalomtípusként támogatja az Application/XML-t.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="5bbd7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbd7-122">-DefaultProfile</span></span>
<span data-ttu-id="5bbd7-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5bbd7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bbd7-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="5bbd7-124">-MapDefinition</span></span>
<span data-ttu-id="5bbd7-125">Az integrációs fiók megfeleltetését megadó objektum.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="5bbd7-126">Adja meg ezt a paramétert vagy a *MapFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="5bbd7-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="5bbd7-127">-MapFilePath</span></span>
<span data-ttu-id="5bbd7-128">Az integrációs fiók megfeleltetése definíciójának fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="5bbd7-129">Adja meg ezt a paramétert vagy a *MapDefinition* paramétert.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="5bbd7-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="5bbd7-130">-MapName</span></span>
<span data-ttu-id="5bbd7-131">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-131">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="5bbd7-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="5bbd7-132">-MapType</span></span>
<span data-ttu-id="5bbd7-133">Az integrációs fiók megfeleltetésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="5bbd7-134">Ez a parancsmag a térkép típusú XSLT-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-134">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbd7-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5bbd7-135">-Metadata</span></span>
<span data-ttu-id="5bbd7-136">A megfeleltetés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-136">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="5bbd7-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bbd7-137">-Name</span></span>
<span data-ttu-id="5bbd7-138">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-138">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="5bbd7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bbd7-139">-ResourceGroupName</span></span>
<span data-ttu-id="5bbd7-140">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-140">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5bbd7-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bbd7-141">-Confirm</span></span>
<span data-ttu-id="5bbd7-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bbd7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bbd7-143">-WhatIf</span></span>
<span data-ttu-id="5bbd7-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bbd7-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bbd7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bbd7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbd7-146">CommonParameters</span></span>
<span data-ttu-id="5bbd7-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bbd7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbd7-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbd7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbd7-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bbd7-149">INPUTS</span></span>

### <span data-ttu-id="5bbd7-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5bbd7-150">System.String</span></span>

## <span data-ttu-id="5bbd7-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bbd7-151">OUTPUTS</span></span>

### <span data-ttu-id="5bbd7-152">Microsoft. Azure. Management. Logic. models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bbd7-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="5bbd7-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bbd7-153">NOTES</span></span>

## <span data-ttu-id="5bbd7-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bbd7-154">RELATED LINKS</span></span>

[<span data-ttu-id="5bbd7-155">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bbd7-155">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="5bbd7-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bbd7-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="5bbd7-157">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bbd7-157">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


