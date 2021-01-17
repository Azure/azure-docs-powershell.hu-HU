---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368394"
---
# <span data-ttu-id="6c951-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6c951-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="6c951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c951-102">SYNOPSIS</span></span>
<span data-ttu-id="6c951-103">Módosítja az integrációs fiók térképét.</span><span class="sxs-lookup"><span data-stu-id="6c951-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="6c951-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c951-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c951-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c951-105">DESCRIPTION</span></span>
<span data-ttu-id="6c951-106">A **Set-AzIntegrationAccountMap** parancsmag módosítja az integrációs fiók térképét.</span><span class="sxs-lookup"><span data-stu-id="6c951-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="6c951-107">Ez a parancsmag egy objektumot ad vissza, amely az integrációs fiók térképét képviseli.</span><span class="sxs-lookup"><span data-stu-id="6c951-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="6c951-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a leképezés nevét.</span><span class="sxs-lookup"><span data-stu-id="6c951-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="6c951-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="6c951-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6c951-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="6c951-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6c951-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="6c951-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6c951-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="6c951-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6c951-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c951-113">EXAMPLES</span></span>

### <span data-ttu-id="6c951-114">1. példa: Integrációs fiók térképének módosítása</span><span class="sxs-lookup"><span data-stu-id="6c951-114">Example 1: Modify an integration account map</span></span>
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

<span data-ttu-id="6c951-115">Ez a parancs módosítja az integrációs fiók leképezését a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6c951-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="6c951-116">A parancs egy korábbi parancs által a $MapContent egy leképezésdefiníciót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="6c951-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="6c951-117">Example 2</span></span>

<span data-ttu-id="6c951-118">Módosítja az integrációs fiók térképét.</span><span class="sxs-lookup"><span data-stu-id="6c951-118">Modifies an integration account map.</span></span> <span data-ttu-id="6c951-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="6c951-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="6c951-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c951-120">PARAMETERS</span></span>

### <span data-ttu-id="6c951-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6c951-121">-ContentType</span></span>
<span data-ttu-id="6c951-122">Megadja az integrációs fiók térképének tartalomtípusát.</span><span class="sxs-lookup"><span data-stu-id="6c951-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="6c951-123">Ez a parancsmag megfeleltetési tartalomtípusként támogatja az alkalmazás/xml formátumot.</span><span class="sxs-lookup"><span data-stu-id="6c951-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="6c951-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c951-124">-DefaultProfile</span></span>
<span data-ttu-id="6c951-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6c951-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c951-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6c951-126">-Force</span></span>
<span data-ttu-id="6c951-127">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="6c951-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c951-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="6c951-128">-MapDefinition</span></span>
<span data-ttu-id="6c951-129">Egy definícióobjektumot ad meg az integrációs fiók leképezésében.</span><span class="sxs-lookup"><span data-stu-id="6c951-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="6c951-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="6c951-130">-MapFilePath</span></span>
<span data-ttu-id="6c951-131">Az integrációs fiók leképezés definíciójának fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="6c951-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="6c951-132">-MapName</span></span>
<span data-ttu-id="6c951-133">Egy integrációs fiók térképének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="6c951-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="6c951-134">-MapType</span></span>
<span data-ttu-id="6c951-135">Az integrációs fiók térképének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="6c951-136">Ez a parancsmag térképtípusként támogatja az Xslt-et.</span><span class="sxs-lookup"><span data-stu-id="6c951-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="6c951-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6c951-137">-Metadata</span></span>
<span data-ttu-id="6c951-138">A leképezés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="6c951-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6c951-139">-Name</span></span>
<span data-ttu-id="6c951-140">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="6c951-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c951-141">-ResourceGroupName</span></span>
<span data-ttu-id="6c951-142">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c951-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6c951-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c951-143">-Confirm</span></span>
<span data-ttu-id="6c951-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6c951-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c951-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c951-145">-WhatIf</span></span>
<span data-ttu-id="6c951-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6c951-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c951-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c951-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c951-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c951-148">CommonParameters</span></span>
<span data-ttu-id="6c951-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c951-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c951-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c951-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c951-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c951-151">INPUTS</span></span>

### <span data-ttu-id="6c951-152">System.String</span><span class="sxs-lookup"><span data-stu-id="6c951-152">System.String</span></span>

## <span data-ttu-id="6c951-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c951-153">OUTPUTS</span></span>

### <span data-ttu-id="6c951-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6c951-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="6c951-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c951-155">NOTES</span></span>

## <span data-ttu-id="6c951-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c951-156">RELATED LINKS</span></span>

[<span data-ttu-id="6c951-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6c951-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="6c951-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6c951-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="6c951-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6c951-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


