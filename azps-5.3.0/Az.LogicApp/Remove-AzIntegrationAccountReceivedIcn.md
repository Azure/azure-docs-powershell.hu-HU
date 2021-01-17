---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469469"
---
# <span data-ttu-id="456d3-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="456d3-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="456d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456d3-102">SYNOPSIS</span></span>
<span data-ttu-id="456d3-103">Ez a parancsmag eltávolít egy konkrét beérkezett adatcsere-vezérlőszámot szerződésenként és vezérlőszámonként.</span><span class="sxs-lookup"><span data-stu-id="456d3-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="456d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="456d3-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="456d3-105">DESCRIPTION</span></span>
<span data-ttu-id="456d3-106">Ezt a parancsmagot katasztrófa-helyreállítási helyzetekben arra szántuk, hogy eltávolítson egy beérkezett adatcsere-vezérlőszámot az integrációs fiókból, hogy a B2B-összekötő ismét feldolgozhatja az üzenetet, ha engedélyezve van a duplikált szám észlelése.</span><span class="sxs-lookup"><span data-stu-id="456d3-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="456d3-107">Ritkán előfordulhat, hogy a kapott csomópontvezérlő számot nem sokkal a katasztrófa előtt lefoglalják, és mielőtt a B2B-összekötő hibásként utasítja el a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="456d3-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="456d3-108">Ilyen esetekben előfordulhat, hogy a művelet lehetővé teszi a helyreállítási webhelynek, hogy a terhelés kijavítása után újra feldolgozzon ugyanazt a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="456d3-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="456d3-109">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="456d3-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="456d3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="456d3-110">EXAMPLES</span></span>

### <span data-ttu-id="456d3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="456d3-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="456d3-112">Olyan, beérkezett X12-es vezérlőszámot kísérl meg beszeretni, amely nem érvényes formátumú.</span><span class="sxs-lookup"><span data-stu-id="456d3-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="456d3-113">Eltávolítja a kapott X12-es adatcserére használható vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="456d3-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="456d3-114">Megerősíti, hogy a kapott X12-es csomópont vezérlőszámát eltávolította úgy, hogy megpróbálja újból megkapni.</span><span class="sxs-lookup"><span data-stu-id="456d3-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="456d3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="456d3-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="456d3-116">Egy beérkezett Edifact interchange vezérlőszám bekért számát kísérli meg megkapni, amely nem érvényes formátumú.</span><span class="sxs-lookup"><span data-stu-id="456d3-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="456d3-117">Eltávolítja a kapott Edifact interchange vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="456d3-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="456d3-118">Megerősíti, hogy a kapott Edifact interchange vezérlőszám el lett távolítva úgy, hogy megpróbálja újból megkapni.</span><span class="sxs-lookup"><span data-stu-id="456d3-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="456d3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="456d3-119">PARAMETERS</span></span>

### <span data-ttu-id="456d3-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="456d3-120">-AgreementName</span></span>
<span data-ttu-id="456d3-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="456d3-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="456d3-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="456d3-122">-AgreementType</span></span>
<span data-ttu-id="456d3-123">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="456d3-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="456d3-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="456d3-124">-ControlNumberValue</span></span>
<span data-ttu-id="456d3-125">Az integrációs fiók vezérlőszámának értéke.</span><span class="sxs-lookup"><span data-stu-id="456d3-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="456d3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456d3-126">-DefaultProfile</span></span>
<span data-ttu-id="456d3-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="456d3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="456d3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="456d3-128">-Name</span></span>
<span data-ttu-id="456d3-129">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="456d3-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="456d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="456d3-131">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="456d3-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="456d3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="456d3-132">-Confirm</span></span>
<span data-ttu-id="456d3-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="456d3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456d3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456d3-134">-WhatIf</span></span>
<span data-ttu-id="456d3-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="456d3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456d3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="456d3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456d3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456d3-137">CommonParameters</span></span>
<span data-ttu-id="456d3-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456d3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456d3-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456d3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456d3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="456d3-140">INPUTS</span></span>

### <span data-ttu-id="456d3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="456d3-141">System.String</span></span>

## <span data-ttu-id="456d3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="456d3-142">OUTPUTS</span></span>

### <span data-ttu-id="456d3-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="456d3-143">System.Void</span></span>

## <span data-ttu-id="456d3-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="456d3-144">NOTES</span></span>

## <span data-ttu-id="456d3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="456d3-145">RELATED LINKS</span></span>

<span data-ttu-id="456d3-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="456d3-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

