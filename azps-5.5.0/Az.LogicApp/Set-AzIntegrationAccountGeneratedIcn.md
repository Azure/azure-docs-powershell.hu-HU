---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154802"
---
# <span data-ttu-id="831ad-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="831ad-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="831ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="831ad-102">SYNOPSIS</span></span>
<span data-ttu-id="831ad-103">Frissíti az integrációs fiók által létrehozott adatcsere-vezérlő számát (ICN) az Azure erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="831ad-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="831ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="831ad-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="831ad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="831ad-105">DESCRIPTION</span></span>
<span data-ttu-id="831ad-106">A Set-AzIntegrationAccountGeneratedIcn parancsmag frissíti a meglévő integrációs fiók által létrehozott adatcsere-vezérlőszámot (ICN), és visszaad egy objektumot, amely az integrációs fiók által létrehozott adatcsere-vezérlő számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="831ad-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="831ad-107">Ezzel a parancsmagmal frissítheti az integrációs fiók által létrehozott adatcsere-vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="831ad-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="831ad-108">Frissítheti az integrációs fiók által létrehozott adatcsere-vezérlő számát az integrációs fiók nevének, az erőforráscsoport nevének és a szerződés nevének megadásával.</span><span class="sxs-lookup"><span data-stu-id="831ad-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="831ad-109">Ezzel a paranccsal nem hozhat létre új integrációs fiók által létrehozott adatcsere-vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="831ad-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="831ad-110">A dinamikus paraméterek csak írja be őket a parancsba, vagy írjon be egy kötőjelet (-) a paraméter nevének jelzésére, majd nyomja le többször a TAB billentyűt az elérhető paraméterek között való váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="831ad-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="831ad-111">Ha nem ad meg egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="831ad-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="831ad-112">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterobjektumában megadott paraméterértékekkel.</span><span class="sxs-lookup"><span data-stu-id="831ad-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="831ad-113">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="831ad-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="831ad-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="831ad-114">EXAMPLES</span></span>

### <span data-ttu-id="831ad-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="831ad-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="831ad-116">Ez a parancs egy adott integrációs fiók szerződésében létrehozott X12-es integrációs fiók vezérlőszámát kapja meg, 100-sal megnöveli az értékét, majd visszaírja a frissített értéket.</span><span class="sxs-lookup"><span data-stu-id="831ad-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="831ad-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="831ad-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="831ad-118">Ez a parancs egy adott integrációs fiók szerződésének EdifactIntegrationAccountAgreement interchange vezérlőszámát kapja meg, 100-sal növeli az értékét, majd visszaírja a frissített értéket.</span><span class="sxs-lookup"><span data-stu-id="831ad-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="831ad-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="831ad-119">PARAMETERS</span></span>

### <span data-ttu-id="831ad-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="831ad-120">-AgreementName</span></span>
<span data-ttu-id="831ad-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="831ad-121">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ad-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="831ad-122">-AgreementType</span></span>
<span data-ttu-id="831ad-123">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="831ad-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ad-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="831ad-124">-ControlNumber</span></span>
<span data-ttu-id="831ad-125">A létrehozott vezérlőszám új értéke.</span><span class="sxs-lookup"><span data-stu-id="831ad-125">The generated control number new value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831ad-126">-DefaultProfile</span></span>
<span data-ttu-id="831ad-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="831ad-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="831ad-128">-Name</span><span class="sxs-lookup"><span data-stu-id="831ad-128">-Name</span></span>
<span data-ttu-id="831ad-129">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="831ad-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831ad-130">-ResourceGroupName</span></span>
<span data-ttu-id="831ad-131">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="831ad-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="831ad-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="831ad-132">-Confirm</span></span>
<span data-ttu-id="831ad-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="831ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="831ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="831ad-134">-WhatIf</span></span>
<span data-ttu-id="831ad-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="831ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="831ad-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="831ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="831ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831ad-137">CommonParameters</span></span>
<span data-ttu-id="831ad-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831ad-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="831ad-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831ad-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="831ad-140">INPUTS</span></span>

### <span data-ttu-id="831ad-141">System.String</span><span class="sxs-lookup"><span data-stu-id="831ad-141">System.String</span></span>

## <span data-ttu-id="831ad-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="831ad-142">OUTPUTS</span></span>

### <span data-ttu-id="831ad-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="831ad-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="831ad-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="831ad-144">NOTES</span></span>

## <span data-ttu-id="831ad-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="831ad-145">RELATED LINKS</span></span>

[<span data-ttu-id="831ad-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="831ad-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

