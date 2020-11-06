---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 2f6df9b28db7ad86a3c779a166df34c48d779621
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505927"
---
# <span data-ttu-id="f3f52-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3f52-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="f3f52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3f52-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f52-103">Az integrációs fiók megfeleltetését hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f3f52-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3f52-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3f52-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f52-106">A **New-AzureRmIntegrationAccountMap** parancsmag létrehoz egy integrációs fiók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="f3f52-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="f3f52-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók megfeleltetését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f3f52-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="f3f52-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét, a megfeleltetés nevét és a Térkép definícióját.</span><span class="sxs-lookup"><span data-stu-id="f3f52-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="f3f52-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="f3f52-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="f3f52-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="f3f52-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f3f52-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="f3f52-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f3f52-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="f3f52-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f3f52-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="f3f52-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f3f52-114">Példák</span><span class="sxs-lookup"><span data-stu-id="f3f52-114">EXAMPLES</span></span>

### <span data-ttu-id="f3f52-115">1. példa: az integrációs fiók megfeleltetésének létrehozása</span><span class="sxs-lookup"><span data-stu-id="f3f52-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="f3f52-116">Ez a parancs létrehozza az integrációs fiók megfeleltetését a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="f3f52-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="f3f52-117">A parancs a $MapContent változóban egy korábbi parancs által tárolt megfeleltetési definíciót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="f3f52-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3f52-118">PARAMETERS</span></span>

### <span data-ttu-id="f3f52-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="f3f52-119">-ContentType</span></span>
<span data-ttu-id="f3f52-120">Az integrációs fiók megfeleltetésének tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="f3f52-121">Ez a parancsmag a térképes tartalomtípusként támogatja az Application/XML-t.</span><span class="sxs-lookup"><span data-stu-id="f3f52-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="f3f52-122">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="f3f52-122">-MapDefinition</span></span>
<span data-ttu-id="f3f52-123">Az integrációs fiók megfeleltetését megadó objektum.</span><span class="sxs-lookup"><span data-stu-id="f3f52-123">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="f3f52-124">Adja meg ezt a paramétert vagy a *MapFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f3f52-124">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="f3f52-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="f3f52-125">-MapFilePath</span></span>
<span data-ttu-id="f3f52-126">Az integrációs fiók megfeleltetése definíciójának fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-126">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="f3f52-127">Adja meg ezt a paramétert vagy a *MapDefinition* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f3f52-127">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="f3f52-128">-MapName</span><span class="sxs-lookup"><span data-stu-id="f3f52-128">-MapName</span></span>
<span data-ttu-id="f3f52-129">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-129">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="f3f52-130">-MapType</span><span class="sxs-lookup"><span data-stu-id="f3f52-130">-MapType</span></span>
<span data-ttu-id="f3f52-131">Az integrációs fiók megfeleltetésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-131">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="f3f52-132">Ez a parancsmag a térkép típusú XSLT-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="f3f52-132">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f52-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f3f52-133">-Metadata</span></span>
<span data-ttu-id="f3f52-134">A megfeleltetés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-134">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="f3f52-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3f52-135">-Name</span></span>
<span data-ttu-id="f3f52-136">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-136">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="f3f52-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f52-137">-ResourceGroupName</span></span>
<span data-ttu-id="f3f52-138">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3f52-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f3f52-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3f52-139">-Confirm</span></span>
<span data-ttu-id="f3f52-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3f52-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f52-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f52-141">-WhatIf</span></span>
<span data-ttu-id="f3f52-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3f52-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f52-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3f52-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f52-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f52-144">-DefaultProfile</span></span>
<span data-ttu-id="f3f52-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3f52-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f52-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f52-146">CommonParameters</span></span>
<span data-ttu-id="f3f52-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3f52-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f52-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f52-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f52-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f52-149">INPUTS</span></span>

## <span data-ttu-id="f3f52-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3f52-150">OUTPUTS</span></span>

### <span data-ttu-id="f3f52-151">Microsoft. Azure. Management. Logic. models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3f52-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="f3f52-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3f52-152">NOTES</span></span>

## <span data-ttu-id="f3f52-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3f52-153">RELATED LINKS</span></span>

[<span data-ttu-id="f3f52-154">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3f52-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="f3f52-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3f52-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="f3f52-156">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3f52-156">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


