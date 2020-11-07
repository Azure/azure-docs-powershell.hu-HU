---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846001"
---
# <span data-ttu-id="dedb6-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="dedb6-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="dedb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dedb6-102">SYNOPSIS</span></span>
<span data-ttu-id="dedb6-103">Ez a parancsmag kikeresi a generált bankközi vezérlő szám aktuális értékét a szerződés alapján.</span><span class="sxs-lookup"><span data-stu-id="dedb6-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="dedb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dedb6-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dedb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dedb6-105">DESCRIPTION</span></span>
<span data-ttu-id="dedb6-106">Ezt a parancsmagot a generált bankközi vezérlő szám aktuális értékének lekérése a katasztrófa-elhárítási helyzetekben a set-AzIntegrationAccountGeneratedIcn értékkel való megnövelt értékre kell használni.</span><span class="sxs-lookup"><span data-stu-id="dedb6-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="dedb6-107">A bankközi vezérlő számát növelni kell annak érdekében, hogy elkerülhető legyen az olyan számok duplikált vezérlési száma, amelyek még nem replikálódtak a passzív területre, amikor az aktív régióban katasztrófa történt.</span><span class="sxs-lookup"><span data-stu-id="dedb6-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="dedb6-108">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="dedb6-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="dedb6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dedb6-109">EXAMPLES</span></span>

### <span data-ttu-id="dedb6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dedb6-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="dedb6-111">Ez a parancs beilleszti az integrációs fiókot, amely a X12-bankközi vezérlő számát a szerződés neve alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="dedb6-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="dedb6-112">Ügyeljen arra, hogy a megadott szerződés típusa "X12" legyen</span><span class="sxs-lookup"><span data-stu-id="dedb6-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="dedb6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="dedb6-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="dedb6-114">Ez a parancs beilleszti az integrációs fiókot, amely a EDIFACT-bankközi vezérlő számát a szerződés neve alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="dedb6-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="dedb6-115">Ügyeljen arra, hogy a megadott szerződés típusa "EDIFACT" legyen</span><span class="sxs-lookup"><span data-stu-id="dedb6-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="dedb6-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="dedb6-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="dedb6-117">Ez a parancs az összes generált X12-vezérlő számot az integrációs fiók nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dedb6-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="dedb6-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dedb6-118">PARAMETERS</span></span>

### <span data-ttu-id="dedb6-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="dedb6-119">-AgreementName</span></span>
<span data-ttu-id="dedb6-120">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="dedb6-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="dedb6-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="dedb6-121">-AgreementType</span></span>
<span data-ttu-id="dedb6-122">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="dedb6-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="dedb6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedb6-123">-DefaultProfile</span></span>
<span data-ttu-id="dedb6-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dedb6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dedb6-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dedb6-125">-Name</span></span>
<span data-ttu-id="dedb6-126">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="dedb6-126">The integration account name.</span></span>

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

### <span data-ttu-id="dedb6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedb6-127">-ResourceGroupName</span></span>
<span data-ttu-id="dedb6-128">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="dedb6-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="dedb6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedb6-129">CommonParameters</span></span>
<span data-ttu-id="dedb6-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dedb6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedb6-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedb6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedb6-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedb6-132">INPUTS</span></span>

### <span data-ttu-id="dedb6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dedb6-133">System.String</span></span>

## <span data-ttu-id="dedb6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedb6-134">OUTPUTS</span></span>

### <span data-ttu-id="dedb6-135">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="dedb6-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="dedb6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dedb6-136">NOTES</span></span>

## <span data-ttu-id="dedb6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dedb6-137">RELATED LINKS</span></span>

[<span data-ttu-id="dedb6-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="dedb6-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

