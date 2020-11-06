---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 04cd6204b93a0ce84f025d6af931c5f5e287c558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498907"
---
# <span data-ttu-id="2f873-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2f873-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="2f873-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f873-102">SYNOPSIS</span></span>
<span data-ttu-id="2f873-103">Az integrációs fiók megfeleltetését módosítja.</span><span class="sxs-lookup"><span data-stu-id="2f873-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f873-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f873-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f873-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f873-105">DESCRIPTION</span></span>
<span data-ttu-id="2f873-106">A **set-AzureRmIntegrationAccountMap** parancsmag az integrációs fiók megfeleltetését módosítja.</span><span class="sxs-lookup"><span data-stu-id="2f873-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="2f873-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók megfeleltetését jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2f873-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="2f873-108">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a megfeleltetés nevét.</span><span class="sxs-lookup"><span data-stu-id="2f873-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="2f873-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="2f873-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2f873-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="2f873-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2f873-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="2f873-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2f873-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="2f873-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2f873-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2f873-113">EXAMPLES</span></span>

### <span data-ttu-id="2f873-114">Példa 1: az integrációs fiók megfeleltetésének módosítása</span><span class="sxs-lookup"><span data-stu-id="2f873-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="2f873-115">Ez a parancs módosítja az integrációs fiók megfeleltetését a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="2f873-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="2f873-116">A parancs a $MapContent változóban egy korábbi parancs által tárolt megfeleltetési definíciót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="2f873-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f873-117">PARAMETERS</span></span>

### <span data-ttu-id="2f873-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="2f873-118">-ContentType</span></span>
<span data-ttu-id="2f873-119">Az integrációs fiók megfeleltetésének tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="2f873-120">Ez a parancsmag a térképes tartalomtípusként támogatja az Application/XML-t.</span><span class="sxs-lookup"><span data-stu-id="2f873-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f873-121">-DefaultProfile</span></span>
<span data-ttu-id="2f873-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f873-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f873-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2f873-123">-Force</span></span>
<span data-ttu-id="2f873-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2f873-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f873-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="2f873-125">-MapDefinition</span></span>
<span data-ttu-id="2f873-126">Az integrációs fiók megfeleltetését megadó objektum.</span><span class="sxs-lookup"><span data-stu-id="2f873-126">Specifies a definition object for integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="2f873-127">-MapFilePath</span></span>
<span data-ttu-id="2f873-128">Az integrációs fiók megfeleltetése definíciójának fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-128">Specifies the file path of a definition for the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="2f873-129">-MapName</span></span>
<span data-ttu-id="2f873-130">Az integrációs fiók megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-130">Specifies the name of an integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="2f873-131">-MapType</span></span>
<span data-ttu-id="2f873-132">Az integrációs fiók megfeleltetésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="2f873-133">Ez a parancsmag a térkép típusú XSLT-t támogatja.</span><span class="sxs-lookup"><span data-stu-id="2f873-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2f873-134">-Metadata</span></span>
<span data-ttu-id="2f873-135">A megfeleltetés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-135">Specifies a metadata object for the map.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f873-136">-Name</span></span>
<span data-ttu-id="2f873-137">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-137">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f873-138">-ResourceGroupName</span></span>
<span data-ttu-id="2f873-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f873-139">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f873-140">-Confirm</span></span>
<span data-ttu-id="2f873-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f873-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f873-142">-WhatIf</span></span>
<span data-ttu-id="2f873-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f873-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f873-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f873-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f873-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f873-145">CommonParameters</span></span>
<span data-ttu-id="2f873-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f873-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f873-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f873-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f873-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f873-148">INPUTS</span></span>

### <span data-ttu-id="2f873-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="2f873-149">None</span></span>
<span data-ttu-id="2f873-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2f873-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f873-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f873-151">OUTPUTS</span></span>

### <span data-ttu-id="2f873-152">Microsoft. Azure. Management. Logic. models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2f873-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="2f873-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f873-153">NOTES</span></span>

## <span data-ttu-id="2f873-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f873-154">RELATED LINKS</span></span>

[<span data-ttu-id="2f873-155">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2f873-155">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="2f873-156">Új – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2f873-156">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="2f873-157">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2f873-157">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


