---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: aacdcaff98e5cb647c5b4fe1988c24dacc040416
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666075"
---
# <span data-ttu-id="d26cb-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="d26cb-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="d26cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d26cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d26cb-103">Ezzel a parancsmaggal egy adott kapott bankközi vezérlőelem-számot, illetve vezérlő számértéket kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="d26cb-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="d26cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d26cb-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d26cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d26cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d26cb-106">Ezt a parancsmagot a beérkezett bankközi vezérlő számának ellenőrzésére szolgáló katasztrófa-helyreállítási helyzetekben kell használni, és tetszés szerint el kell távolítania az entitást az eltávolítási AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="d26cb-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="d26cb-107">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="d26cb-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="d26cb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d26cb-108">EXAMPLES</span></span>

### <span data-ttu-id="d26cb-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d26cb-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="d26cb-110">Ez a parancs a X12-integrációs fiókot kapja meg a szerződés neve és az ellenőrzés száma mezőben.</span><span class="sxs-lookup"><span data-stu-id="d26cb-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="d26cb-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="d26cb-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="d26cb-112">Ez a parancs a EDIFACT-integrációs fiókot kapja meg a szerződés neve és az ellenőrzés száma mezőben.</span><span class="sxs-lookup"><span data-stu-id="d26cb-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="d26cb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d26cb-113">PARAMETERS</span></span>

### <span data-ttu-id="d26cb-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d26cb-114">-AgreementName</span></span>
<span data-ttu-id="d26cb-115">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="d26cb-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="d26cb-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d26cb-116">-AgreementType</span></span>
<span data-ttu-id="d26cb-117">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="d26cb-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="d26cb-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="d26cb-118">-ControlNumberValue</span></span>
<span data-ttu-id="d26cb-119">Az integrációs fiók vezérlőelemének számértéke.</span><span class="sxs-lookup"><span data-stu-id="d26cb-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="d26cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26cb-120">-DefaultProfile</span></span>
<span data-ttu-id="d26cb-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d26cb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d26cb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d26cb-122">-Name</span></span>
<span data-ttu-id="d26cb-123">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d26cb-123">The integration account name.</span></span>

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

### <span data-ttu-id="d26cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d26cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="d26cb-125">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d26cb-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="d26cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26cb-126">CommonParameters</span></span>
<span data-ttu-id="d26cb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d26cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26cb-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d26cb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26cb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26cb-129">INPUTS</span></span>

### <span data-ttu-id="d26cb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d26cb-130">System.String</span></span>

## <span data-ttu-id="d26cb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26cb-131">OUTPUTS</span></span>

### <span data-ttu-id="d26cb-132">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="d26cb-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="d26cb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d26cb-133">NOTES</span></span>

## <span data-ttu-id="d26cb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d26cb-134">RELATED LINKS</span></span>

[<span data-ttu-id="d26cb-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="d26cb-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="d26cb-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="d26cb-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
