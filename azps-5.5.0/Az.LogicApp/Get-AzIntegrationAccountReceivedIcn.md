---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154858"
---
# <span data-ttu-id="393dd-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="393dd-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="393dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="393dd-102">SYNOPSIS</span></span>
<span data-ttu-id="393dd-103">Ez a parancsmag szerződésenként és vezérlőszámonként egy adott beérkezett adatcsere-vezérlőszámot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="393dd-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="393dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="393dd-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="393dd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="393dd-105">DESCRIPTION</span></span>
<span data-ttu-id="393dd-106">Ezt a parancsmagot katasztrófa-helyreállítási helyzetekben arra szántuk, hogy érvényesítse egy beérkezett adatcsere-vezérlőszám jelenlétét, és szükség esetén távolítsa el az entitást a Remove-AzIntegrationAccountReceivedIcn parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="393dd-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="393dd-107">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="393dd-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="393dd-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="393dd-108">EXAMPLES</span></span>

### <span data-ttu-id="393dd-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="393dd-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="393dd-110">Ez a parancs az X12-es integrációs fiók átváltási vezérlőszámát kapja meg szerződésnév és vezérlőszámérték alapján.</span><span class="sxs-lookup"><span data-stu-id="393dd-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="393dd-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="393dd-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="393dd-112">Ez a parancs az Edifact-integrációs fiókot szerződésnév és vezérlőszámérték alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="393dd-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="393dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="393dd-113">PARAMETERS</span></span>

### <span data-ttu-id="393dd-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="393dd-114">-AgreementName</span></span>
<span data-ttu-id="393dd-115">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="393dd-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="393dd-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="393dd-116">-AgreementType</span></span>
<span data-ttu-id="393dd-117">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="393dd-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="393dd-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="393dd-118">-ControlNumberValue</span></span>
<span data-ttu-id="393dd-119">Az integrációs fiók vezérlőszámának értéke.</span><span class="sxs-lookup"><span data-stu-id="393dd-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="393dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393dd-120">-DefaultProfile</span></span>
<span data-ttu-id="393dd-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="393dd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="393dd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="393dd-122">-Name</span></span>
<span data-ttu-id="393dd-123">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="393dd-123">The integration account name.</span></span>

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

### <span data-ttu-id="393dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="393dd-125">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="393dd-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="393dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393dd-126">CommonParameters</span></span>
<span data-ttu-id="393dd-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393dd-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393dd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393dd-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="393dd-129">INPUTS</span></span>

### <span data-ttu-id="393dd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="393dd-130">System.String</span></span>

## <span data-ttu-id="393dd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="393dd-131">OUTPUTS</span></span>

### <span data-ttu-id="393dd-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="393dd-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="393dd-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="393dd-133">NOTES</span></span>

## <span data-ttu-id="393dd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="393dd-134">RELATED LINKS</span></span>

[<span data-ttu-id="393dd-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="393dd-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="393dd-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="393dd-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
