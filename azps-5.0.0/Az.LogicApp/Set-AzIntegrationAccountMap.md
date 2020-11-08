---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195835"
---
# <span data-ttu-id="c0653-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c0653-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="c0653-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0653-102">SYNOPSIS</span></span>
<span data-ttu-id="c0653-103">Az integrációs fiók megfeleltetését módosítja.</span><span class="sxs-lookup"><span data-stu-id="c0653-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="c0653-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0653-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0653-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0653-105">DESCRIPTION</span></span>
<span data-ttu-id="c0653-106">A **set-AzIntegrationAccountMap** parancsmag az integrációs fiók megfeleltetését módosítja.</span><span class="sxs-lookup"><span data-stu-id="c0653-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="c0653-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók megfeleltetését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c0653-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="c0653-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a megfeleltetés nevét.</span><span class="sxs-lookup"><span data-stu-id="c0653-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="c0653-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="c0653-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c0653-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="c0653-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c0653-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="c0653-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c0653-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="c0653-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c0653-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c0653-113">EXAMPLES</span></span>

### <span data-ttu-id="c0653-114">Példa 1: az integrációs fiók megfeleltetésének módosítása</span><span class="sxs-lookup"><span data-stu-id="c0653-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="c0653-115">Ez a parancs módosítja az integrációs fiók megfeleltetését a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="c0653-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="c0653-116">A parancs a $MapContent változóban egy korábbi parancs által tárolt megfeleltetési definíciót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="c0653-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="c0653-117">Example 2</span></span>

<span data-ttu-id="c0653-118">Az integrációs fiók megfeleltetését módosítja.</span><span class="sxs-lookup"><span data-stu-id="c0653-118">Modifies an integration account map.</span></span> <span data-ttu-id="c0653-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="c0653-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="c0653-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0653-120">PARAMETERS</span></span>

### <span data-ttu-id="c0653-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="c0653-121">-ContentType</span></span>
<span data-ttu-id="c0653-122">Az integrációs fiók megfeleltetésének tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="c0653-123">Ez a parancsmag a térképes tartalomtípusként támogatja az Application/XML-t.</span><span class="sxs-lookup"><span data-stu-id="c0653-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="c0653-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0653-124">-DefaultProfile</span></span>
<span data-ttu-id="c0653-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0653-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0653-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c0653-126">-Force</span></span>
<span data-ttu-id="c0653-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c0653-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0653-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="c0653-128">-MapDefinition</span></span>
<span data-ttu-id="c0653-129">Az integrációs fiók megfeleltetését megadó objektum.</span><span class="sxs-lookup"><span data-stu-id="c0653-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="c0653-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="c0653-130">-MapFilePath</span></span>
<span data-ttu-id="c0653-131">Az integrációs fiók megfeleltetése definíciójának fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="c0653-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="c0653-132">-MapName</span></span>
<span data-ttu-id="c0653-133">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="c0653-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="c0653-134">-MapType</span></span>
<span data-ttu-id="c0653-135">Az integrációs fiók megfeleltetésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="c0653-136">Ez a parancsmag a térkép típusú XSLT-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="c0653-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="c0653-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c0653-137">-Metadata</span></span>
<span data-ttu-id="c0653-138">A megfeleltetés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="c0653-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0653-139">-Name</span></span>
<span data-ttu-id="c0653-140">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="c0653-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0653-141">-ResourceGroupName</span></span>
<span data-ttu-id="c0653-142">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0653-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c0653-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0653-143">-Confirm</span></span>
<span data-ttu-id="c0653-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0653-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0653-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0653-145">-WhatIf</span></span>
<span data-ttu-id="c0653-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0653-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0653-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0653-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0653-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0653-148">CommonParameters</span></span>
<span data-ttu-id="c0653-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0653-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0653-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0653-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0653-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0653-151">INPUTS</span></span>

### <span data-ttu-id="c0653-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c0653-152">System.String</span></span>

## <span data-ttu-id="c0653-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0653-153">OUTPUTS</span></span>

### <span data-ttu-id="c0653-154">Microsoft. Azure. Management. Logic. models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c0653-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="c0653-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0653-155">NOTES</span></span>

## <span data-ttu-id="c0653-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0653-156">RELATED LINKS</span></span>

[<span data-ttu-id="c0653-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c0653-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="c0653-158">Új – AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c0653-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="c0653-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c0653-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


