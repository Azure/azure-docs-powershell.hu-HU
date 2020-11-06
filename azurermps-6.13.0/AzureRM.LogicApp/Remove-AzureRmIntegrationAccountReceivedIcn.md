---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 429c2eefb9c5ba69b829e292522d168939170e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497403"
---
# <span data-ttu-id="83898-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="83898-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="83898-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83898-102">SYNOPSIS</span></span>
<span data-ttu-id="83898-103">Ez a parancsmag eltávolítja a kapott bankközi vezérlőelem-számot egy szerződésben, és szabályozza a számértéket.</span><span class="sxs-lookup"><span data-stu-id="83898-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83898-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83898-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83898-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83898-105">DESCRIPTION</span></span>
<span data-ttu-id="83898-106">Ezt a parancsmagot arra érdemes használni, hogy katasztrófa-helyreállítási helyzetekben el lehessen távolítani a beérkezett bankközi vezérlő számát az integrációs fiókból úgy, hogy a VÁLLALATKÖZI összekötő újra feldolgozza az üzenetet, amikor az ismétlődő számok észlelése engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="83898-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="83898-107">Ritka esetekben előfordulhat, hogy a kapott bankközi vezérlő száma röviddel a katasztrófa előtt van fenntartva, és a VÁLLALATKÖZI összekötő elutasítja a cserét hibásként.</span><span class="sxs-lookup"><span data-stu-id="83898-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="83898-108">Az ilyen alkalmakkor a művelet lehetővé teszi, hogy a helyreállítási webhelye ismét ugyanazzal a csomóponttal dolgozza fel a tartalmat, miután kijavította a tartalmat.</span><span class="sxs-lookup"><span data-stu-id="83898-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="83898-109">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="83898-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="83898-110">Példák</span><span class="sxs-lookup"><span data-stu-id="83898-110">EXAMPLES</span></span>

### <span data-ttu-id="83898-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83898-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="83898-112">Megkísérli beszerezni a beérkezett X12-adatcsere vezérlő számát, hogy a tartalom nem érvényes formátumú-e.</span><span class="sxs-lookup"><span data-stu-id="83898-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="83898-113">Eltávolítja a beérkezett X12 bankközi vezérlő számát.</span><span class="sxs-lookup"><span data-stu-id="83898-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="83898-114">Megerősíti a kapott X12-as bankközi vezérlő számát azzal, hogy megpróbálja újra bekapcsolódni.</span><span class="sxs-lookup"><span data-stu-id="83898-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="83898-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="83898-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="83898-116">Megkísérli beszerezni a beérkezett EDIFACT-adatcsere vezérlő számát, hogy a tartalom nem érvényes formátumú-e.</span><span class="sxs-lookup"><span data-stu-id="83898-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="83898-117">Eltávolítja a beérkezett EDIFACT bankközi vezérlő számát.</span><span class="sxs-lookup"><span data-stu-id="83898-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="83898-118">Megerősíti a kapott EDIFACT-as bankközi vezérlő számát azzal, hogy megpróbálja újra bekapcsolódni.</span><span class="sxs-lookup"><span data-stu-id="83898-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="83898-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83898-119">PARAMETERS</span></span>

### <span data-ttu-id="83898-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="83898-120">-AgreementName</span></span>
<span data-ttu-id="83898-121">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="83898-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="83898-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="83898-122">-AgreementType</span></span>
<span data-ttu-id="83898-123">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="83898-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="83898-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="83898-124">-ControlNumberValue</span></span>
<span data-ttu-id="83898-125">Az integrációs fiók vezérlőelemének számértéke.</span><span class="sxs-lookup"><span data-stu-id="83898-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="83898-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83898-126">-DefaultProfile</span></span>
<span data-ttu-id="83898-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="83898-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83898-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83898-128">-Name</span></span>
<span data-ttu-id="83898-129">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="83898-129">The integration account name.</span></span>

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

### <span data-ttu-id="83898-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83898-130">-ResourceGroupName</span></span>
<span data-ttu-id="83898-131">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="83898-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="83898-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83898-132">-Confirm</span></span>
<span data-ttu-id="83898-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83898-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83898-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83898-134">-WhatIf</span></span>
<span data-ttu-id="83898-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83898-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83898-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83898-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83898-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83898-137">CommonParameters</span></span>
<span data-ttu-id="83898-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83898-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83898-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83898-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83898-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83898-140">INPUTS</span></span>

### <span data-ttu-id="83898-141">System. String</span><span class="sxs-lookup"><span data-stu-id="83898-141">System.String</span></span>

## <span data-ttu-id="83898-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83898-142">OUTPUTS</span></span>

### <span data-ttu-id="83898-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="83898-143">System.Void</span></span>

## <span data-ttu-id="83898-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83898-144">NOTES</span></span>

## <span data-ttu-id="83898-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83898-145">RELATED LINKS</span></span>

<span data-ttu-id="83898-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="83898-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

