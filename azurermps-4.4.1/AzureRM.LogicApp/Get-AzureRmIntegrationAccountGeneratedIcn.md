---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 2855f5da15de776d7fd85bd267f6a082a85ba5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493473"
---
# <span data-ttu-id="1d4f5-101">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="1d4f5-101">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="1d4f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4f5-103">Ez a parancsmag kikeresi a generált bankközi vezérlő szám aktuális értékét a szerződés alapján.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d4f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d4f5-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d4f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d4f5-105">DESCRIPTION</span></span>
<span data-ttu-id="1d4f5-106">Ezt a parancsmagot a generált bankközi vezérlő szám aktuális értékének lekérése a katasztrófa-elhárítási helyzetekben a set-AzureRmIntegrationAccountGeneratedIcn értékkel való megnövelt értékre kell használni.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzureRmIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="1d4f5-107">A bankközi vezérlő számát növelni kell annak érdekében, hogy elkerülhető legyen az olyan számok duplikált vezérlési száma, amelyek még nem replikálódtak a passzív területre, amikor az aktív régióban katasztrófa történt.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="1d4f5-108">Kérjük, adja meg a "-AgreementType" paramétert annak megadásához, hogy a X12 vagy a EDIFACT vezérlő számokat adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="1d4f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d4f5-109">EXAMPLES</span></span>

### <span data-ttu-id="1d4f5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d4f5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="1d4f5-111">Ez a parancs beilleszti az integrációs fiókot, amely a X12-bankközi vezérlő számát a szerződés neve alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="1d4f5-112">Ügyeljen arra, hogy a megadott szerződés típusa "X12" legyen</span><span class="sxs-lookup"><span data-stu-id="1d4f5-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="1d4f5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1d4f5-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="1d4f5-114">Ez a parancs beilleszti az integrációs fiókot, amely a EDIFACT-bankközi vezérlő számát a szerződés neve alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="1d4f5-115">Ügyeljen arra, hogy a megadott szerződés típusa "EDIFACT" legyen</span><span class="sxs-lookup"><span data-stu-id="1d4f5-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="1d4f5-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="1d4f5-116">Example 3</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
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

<span data-ttu-id="1d4f5-117">Ez a parancs az összes generált X12-vezérlő számot az integrációs fiók nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="1d4f5-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d4f5-118">PARAMETERS</span></span>

### <span data-ttu-id="1d4f5-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="1d4f5-119">-AgreementName</span></span>
<span data-ttu-id="1d4f5-120">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="1d4f5-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d4f5-121">-Name</span></span>
<span data-ttu-id="1d4f5-122">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-122">The integration account name.</span></span>

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

### <span data-ttu-id="1d4f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d4f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d4f5-124">Az integrációs fiók erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-124">The integration account resource group name.</span></span>

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

### <span data-ttu-id="1d4f5-125">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="1d4f5-125">-AgreementType</span></span>
<span data-ttu-id="1d4f5-126">Az integrációs fiók szerződés típusa.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-126">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d4f5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4f5-127">-DefaultProfile</span></span>
<span data-ttu-id="1d4f5-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d4f5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d4f5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4f5-129">CommonParameters</span></span>
<span data-ttu-id="1d4f5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d4f5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4f5-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d4f5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4f5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d4f5-132">INPUTS</span></span>

### <span data-ttu-id="1d4f5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1d4f5-133">System.String</span></span>

## <span data-ttu-id="1d4f5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d4f5-134">OUTPUTS</span></span>

### <span data-ttu-id="1d4f5-135">Microsoft. Azure. Command. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="1d4f5-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="1d4f5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d4f5-136">NOTES</span></span>

## <span data-ttu-id="1d4f5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d4f5-137">RELATED LINKS</span></span>

[<span data-ttu-id="1d4f5-138">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="1d4f5-138">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Set-AzureRmIntegrationAccountGeneratedIcn.md)

