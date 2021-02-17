---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147626"
---
# <span data-ttu-id="20880-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="20880-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="20880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20880-102">SYNOPSIS</span></span>
<span data-ttu-id="20880-103">Ez a parancsmag szerződésenként beolvassa a létrehozott adatcserék vezérlőszámának aktuális értékét.</span><span class="sxs-lookup"><span data-stu-id="20880-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="20880-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20880-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20880-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20880-105">DESCRIPTION</span></span>
<span data-ttu-id="20880-106">Ezt a parancsmagot katasztrófa-helyreállítási helyzetekben arra szántuk, hogy beolvassa a létrehozott csomópont-vezérlőszám aktuális értékét, így a Set-AzIntegrationAccountGeneratedIcn segítségével magasabb értéket írjon vissza.</span><span class="sxs-lookup"><span data-stu-id="20880-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="20880-107">A csomópontvezérlő számát növelni kell annak érdekében, hogy elkerülje az ismétlődő adatcsere-vezérlőszámokat azon számok esetén, amelyek még nem replikálhatók a passzív régióba, amikor a katasztrófa az aktív régióban történt.</span><span class="sxs-lookup"><span data-stu-id="20880-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="20880-108">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="20880-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="20880-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20880-109">EXAMPLES</span></span>

### <span data-ttu-id="20880-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="20880-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="20880-111">Ez a parancs a létrehozott X12-es integrációs fiók vezérlőszámát kapja meg szerződésnév szerint.</span><span class="sxs-lookup"><span data-stu-id="20880-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="20880-112">Győződjön meg arról, hogy a megadott szerződés típusa "X12"</span><span class="sxs-lookup"><span data-stu-id="20880-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="20880-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="20880-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="20880-114">Ez a parancs az integrációs fiók által létrehozott Edifact interchange control number (Edifact interchange control number) szerződésnév szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="20880-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="20880-115">Győződjön meg arról, hogy a megadott szerződés típusa "Edifact"</span><span class="sxs-lookup"><span data-stu-id="20880-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="20880-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="20880-116">Example 3</span></span>
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

<span data-ttu-id="20880-117">Ez a parancs az összes létrehozott X12-es vezérlőszámot az integrációs fiók neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="20880-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="20880-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20880-118">PARAMETERS</span></span>

### <span data-ttu-id="20880-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="20880-119">-AgreementName</span></span>
<span data-ttu-id="20880-120">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="20880-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="20880-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="20880-121">-AgreementType</span></span>
<span data-ttu-id="20880-122">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="20880-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="20880-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20880-123">-DefaultProfile</span></span>
<span data-ttu-id="20880-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="20880-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20880-125">-Name</span><span class="sxs-lookup"><span data-stu-id="20880-125">-Name</span></span>
<span data-ttu-id="20880-126">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="20880-126">The integration account name.</span></span>

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

### <span data-ttu-id="20880-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20880-127">-ResourceGroupName</span></span>
<span data-ttu-id="20880-128">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="20880-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="20880-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20880-129">CommonParameters</span></span>
<span data-ttu-id="20880-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20880-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20880-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20880-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20880-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20880-132">INPUTS</span></span>

### <span data-ttu-id="20880-133">System.String</span><span class="sxs-lookup"><span data-stu-id="20880-133">System.String</span></span>

## <span data-ttu-id="20880-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20880-134">OUTPUTS</span></span>

### <span data-ttu-id="20880-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="20880-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="20880-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20880-136">NOTES</span></span>

## <span data-ttu-id="20880-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20880-137">RELATED LINKS</span></span>

[<span data-ttu-id="20880-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="20880-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

