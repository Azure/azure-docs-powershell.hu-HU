---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154794"
---
# <span data-ttu-id="3e228-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e228-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="3e228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e228-102">SYNOPSIS</span></span>
<span data-ttu-id="3e228-103">Módosít egy integrációs partnert.</span><span class="sxs-lookup"><span data-stu-id="3e228-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="3e228-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e228-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e228-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e228-105">DESCRIPTION</span></span>
<span data-ttu-id="3e228-106">A **Set-AzIntegrationAccountPartner** parancsmag módosít egy integrációs partnert.</span><span class="sxs-lookup"><span data-stu-id="3e228-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="3e228-107">Ez a parancsmag egy objektumot ad vissza, amely az integrációs fiók partnerét képviseli.</span><span class="sxs-lookup"><span data-stu-id="3e228-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="3e228-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a partner nevét.</span><span class="sxs-lookup"><span data-stu-id="3e228-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="3e228-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="3e228-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3e228-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="3e228-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3e228-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="3e228-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3e228-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="3e228-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3e228-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e228-113">EXAMPLES</span></span>

### <span data-ttu-id="3e228-114">1. példa: Integrációs fiók partnerének módosítása</span><span class="sxs-lookup"><span data-stu-id="3e228-114">Example 1: Modify an integration account partner</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="3e228-115">Ez a parancs módosítja az IntegrationAccountPartner22 nevű integrációs partnert a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3e228-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="3e228-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="3e228-116">Example 2</span></span>

<span data-ttu-id="3e228-117">Módosít egy integrációs partnert.</span><span class="sxs-lookup"><span data-stu-id="3e228-117">Modifies an integration account partner.</span></span> <span data-ttu-id="3e228-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="3e228-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="3e228-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e228-119">PARAMETERS</span></span>

### <span data-ttu-id="3e228-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="3e228-120">-BusinessIdentities</span></span>
<span data-ttu-id="3e228-121">Megadja az integrációs fiók partnerének üzleti identitását.</span><span class="sxs-lookup"><span data-stu-id="3e228-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="3e228-122">Adjon meg egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="3e228-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="3e228-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e228-123">-DefaultProfile</span></span>
<span data-ttu-id="3e228-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3e228-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e228-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3e228-125">-Force</span></span>
<span data-ttu-id="3e228-126">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3e228-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e228-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3e228-127">-Metadata</span></span>
<span data-ttu-id="3e228-128">A partner metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e228-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="3e228-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3e228-129">-Name</span></span>
<span data-ttu-id="3e228-130">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e228-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3e228-131">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="3e228-131">-PartnerName</span></span>
<span data-ttu-id="3e228-132">Az integrációs fiók partnerének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e228-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="3e228-133">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="3e228-133">-PartnerType</span></span>
<span data-ttu-id="3e228-134">Az integrációs fiók típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3e228-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="3e228-135">Ez a paraméter a B2B típust támogatja.</span><span class="sxs-lookup"><span data-stu-id="3e228-135">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e228-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e228-136">-ResourceGroupName</span></span>
<span data-ttu-id="3e228-137">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e228-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3e228-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e228-138">-Confirm</span></span>
<span data-ttu-id="3e228-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e228-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e228-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e228-140">-WhatIf</span></span>
<span data-ttu-id="3e228-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e228-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e228-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e228-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e228-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e228-143">CommonParameters</span></span>
<span data-ttu-id="3e228-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e228-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e228-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e228-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e228-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e228-146">INPUTS</span></span>

### <span data-ttu-id="3e228-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3e228-147">System.String</span></span>

## <span data-ttu-id="3e228-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e228-148">OUTPUTS</span></span>

### <span data-ttu-id="3e228-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e228-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="3e228-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e228-150">NOTES</span></span>

## <span data-ttu-id="3e228-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e228-151">RELATED LINKS</span></span>

[<span data-ttu-id="3e228-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e228-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3e228-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e228-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3e228-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e228-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


