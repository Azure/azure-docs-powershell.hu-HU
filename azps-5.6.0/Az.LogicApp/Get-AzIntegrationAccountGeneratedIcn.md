---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b6bf2c126a1009d824ab8bae1ea2e2031459d876
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922921"
---
# <span data-ttu-id="d53c6-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="d53c6-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="d53c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d53c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d53c6-103">Ez a parancsmag szerződésenként beolvassa a létrehozott adatcserék vezérlőszámának aktuális értékét.</span><span class="sxs-lookup"><span data-stu-id="d53c6-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="d53c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d53c6-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d53c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d53c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d53c6-106">Ezt a parancsmagot katasztrófa-helyreállítási helyzetekben arra szántuk, hogy beolvassa a létrehozott csomópont-vezérlőszám aktuális értékét, így a Set-AzIntegrationAccountGeneratedIcn segítségével magasabb értéket írjon vissza.</span><span class="sxs-lookup"><span data-stu-id="d53c6-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="d53c6-107">A csomópontvezérlő számát növelni kell annak érdekében, hogy elkerülje az ismétlődő adatcsere-vezérlőszámokat azon számok esetén, amelyek még nem replikálhatók a passzív régióba, amikor a katasztrófa az aktív régióban történt.</span><span class="sxs-lookup"><span data-stu-id="d53c6-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="d53c6-108">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="d53c6-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="d53c6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d53c6-109">EXAMPLES</span></span>

### <span data-ttu-id="d53c6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d53c6-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="d53c6-111">Ez a parancs a létrehozott X12-es integrációs fiók vezérlőszámát kapja meg szerződésnév alapján.</span><span class="sxs-lookup"><span data-stu-id="d53c6-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="d53c6-112">Győződjön meg arról, hogy a megadott szerződés típusa "X12"</span><span class="sxs-lookup"><span data-stu-id="d53c6-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="d53c6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d53c6-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="d53c6-114">Ez a parancs az integrációs fiók által létrehozott Edifact interchange control number (Edifact interchange control number) szerződésnév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d53c6-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="d53c6-115">Győződjön meg arról, hogy a megadott szerződés típusa "Edifact"</span><span class="sxs-lookup"><span data-stu-id="d53c6-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="d53c6-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="d53c6-116">Example 3</span></span>
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

<span data-ttu-id="d53c6-117">Ez a parancs az integrációs fiók neve alapján beszeri az összes létrehozott X12-es vezérlőszámot.</span><span class="sxs-lookup"><span data-stu-id="d53c6-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="d53c6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d53c6-118">PARAMETERS</span></span>

### <span data-ttu-id="d53c6-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d53c6-119">-AgreementName</span></span>
<span data-ttu-id="d53c6-120">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="d53c6-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="d53c6-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d53c6-121">-AgreementType</span></span>
<span data-ttu-id="d53c6-122">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="d53c6-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="d53c6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53c6-123">-DefaultProfile</span></span>
<span data-ttu-id="d53c6-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d53c6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d53c6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d53c6-125">-Name</span></span>
<span data-ttu-id="d53c6-126">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d53c6-126">The integration account name.</span></span>

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

### <span data-ttu-id="d53c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d53c6-128">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="d53c6-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="d53c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53c6-129">CommonParameters</span></span>
<span data-ttu-id="d53c6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53c6-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53c6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53c6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d53c6-132">INPUTS</span></span>

### <span data-ttu-id="d53c6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d53c6-133">System.String</span></span>

## <span data-ttu-id="d53c6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53c6-134">OUTPUTS</span></span>

### <span data-ttu-id="d53c6-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="d53c6-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="d53c6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d53c6-136">NOTES</span></span>

## <span data-ttu-id="d53c6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d53c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="d53c6-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="d53c6-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

