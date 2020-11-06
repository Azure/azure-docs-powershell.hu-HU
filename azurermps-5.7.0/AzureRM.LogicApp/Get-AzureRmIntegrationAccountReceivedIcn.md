---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d3f5b8a00bed15f7b5fa36fc0bd1a016517eeb89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500552"
---
# <span data-ttu-id="19108-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="19108-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="19108-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19108-102">SYNOPSIS</span></span>
<span data-ttu-id="19108-103">Ezzel a parancsmaggal egy adott kapott bankközi vezérlőelem-számot, illetve vezérlő számértéket kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="19108-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19108-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19108-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19108-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19108-105">DESCRIPTION</span></span>
<span data-ttu-id="19108-106">Ezt a parancsmagot a beérkezett bankközi vezérlő számának ellenőrzésére szolgáló katasztrófa-helyreállítási helyzetekben kell használni, és tetszés szerint el kell távolítania az entitást az eltávolítási AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="19108-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="19108-107">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="19108-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="19108-108">Példák</span><span class="sxs-lookup"><span data-stu-id="19108-108">EXAMPLES</span></span>

### <span data-ttu-id="19108-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19108-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="19108-110">Ez a parancs a X12-integrációs fiókot kapja meg a szerződés neve és az ellenőrzés száma mezőben.</span><span class="sxs-lookup"><span data-stu-id="19108-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="19108-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="19108-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="19108-112">Ez a parancs a EDIFACT-integrációs fiókot kapja meg a szerződés neve és az ellenőrzés száma mezőben.</span><span class="sxs-lookup"><span data-stu-id="19108-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="19108-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19108-113">PARAMETERS</span></span>

### <span data-ttu-id="19108-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="19108-114">-AgreementName</span></span>
<span data-ttu-id="19108-115">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="19108-115">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19108-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="19108-116">-AgreementType</span></span>
<span data-ttu-id="19108-117">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="19108-117">The integration account agreement type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19108-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="19108-118">-ControlNumberValue</span></span>
<span data-ttu-id="19108-119">Az integrációs fiók vezérlőelemének számértéke.</span><span class="sxs-lookup"><span data-stu-id="19108-119">The integration account control number value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19108-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19108-120">-DefaultProfile</span></span>
<span data-ttu-id="19108-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19108-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19108-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19108-122">-Name</span></span>
<span data-ttu-id="19108-123">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="19108-123">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19108-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19108-124">-ResourceGroupName</span></span>
<span data-ttu-id="19108-125">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="19108-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="19108-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19108-126">CommonParameters</span></span>
<span data-ttu-id="19108-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19108-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19108-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19108-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19108-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19108-129">INPUTS</span></span>

### <span data-ttu-id="19108-130">System. String</span><span class="sxs-lookup"><span data-stu-id="19108-130">System.String</span></span>

## <span data-ttu-id="19108-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19108-131">OUTPUTS</span></span>

### <span data-ttu-id="19108-132">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="19108-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="19108-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19108-133">NOTES</span></span>

## <span data-ttu-id="19108-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19108-134">RELATED LINKS</span></span>

[<span data-ttu-id="19108-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="19108-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="19108-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="19108-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
