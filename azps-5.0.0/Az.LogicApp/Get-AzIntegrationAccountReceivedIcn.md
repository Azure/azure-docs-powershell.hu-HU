---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195876"
---
# <span data-ttu-id="f618f-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="f618f-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="f618f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f618f-102">SYNOPSIS</span></span>
<span data-ttu-id="f618f-103">Ezzel a parancsmaggal egy adott kapott bankközi vezérlőelem-számot, illetve vezérlő számértéket kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="f618f-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="f618f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f618f-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f618f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f618f-105">DESCRIPTION</span></span>
<span data-ttu-id="f618f-106">Ezt a parancsmagot a beérkezett bankközi vezérlő számának ellenőrzésére szolgáló katasztrófa-helyreállítási helyzetekben kell használni, és tetszés szerint el kell távolítania az entitást az eltávolítási AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="f618f-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="f618f-107">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="f618f-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="f618f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f618f-108">EXAMPLES</span></span>

### <span data-ttu-id="f618f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f618f-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="f618f-110">Ez a parancs a X12-integrációs fiókot kapja meg a szerződés neve és az ellenőrzés száma mezőben.</span><span class="sxs-lookup"><span data-stu-id="f618f-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="f618f-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="f618f-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="f618f-112">Ez a parancs a EDIFACT-integrációs fiókot kapja meg a szerződés neve és az ellenőrzés száma mezőben.</span><span class="sxs-lookup"><span data-stu-id="f618f-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="f618f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f618f-113">PARAMETERS</span></span>

### <span data-ttu-id="f618f-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f618f-114">-AgreementName</span></span>
<span data-ttu-id="f618f-115">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="f618f-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="f618f-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f618f-116">-AgreementType</span></span>
<span data-ttu-id="f618f-117">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="f618f-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="f618f-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="f618f-118">-ControlNumberValue</span></span>
<span data-ttu-id="f618f-119">Az integrációs fiók vezérlőelemének számértéke.</span><span class="sxs-lookup"><span data-stu-id="f618f-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="f618f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f618f-120">-DefaultProfile</span></span>
<span data-ttu-id="f618f-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f618f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f618f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f618f-122">-Name</span></span>
<span data-ttu-id="f618f-123">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f618f-123">The integration account name.</span></span>

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

### <span data-ttu-id="f618f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f618f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f618f-125">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f618f-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="f618f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f618f-126">CommonParameters</span></span>
<span data-ttu-id="f618f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f618f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f618f-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f618f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f618f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f618f-129">INPUTS</span></span>

### <span data-ttu-id="f618f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f618f-130">System.String</span></span>

## <span data-ttu-id="f618f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f618f-131">OUTPUTS</span></span>

### <span data-ttu-id="f618f-132">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="f618f-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="f618f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f618f-133">NOTES</span></span>

## <span data-ttu-id="f618f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f618f-134">RELATED LINKS</span></span>

[<span data-ttu-id="f618f-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="f618f-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="f618f-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="f618f-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)