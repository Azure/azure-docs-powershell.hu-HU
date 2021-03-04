---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: df7266548b616615fa45131c21f40622894ffe9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922905"
---
# <span data-ttu-id="c1fd5-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c1fd5-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c1fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fd5-103">Ez a parancsmag szerződésenként és vezérlőszámonként egy adott beérkezett adatcsere-vezérlőszámot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="c1fd5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1fd5-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1fd5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="c1fd5-106">Ezt a parancsmagot katasztrófa-helyreállítási helyzetekben arra szántuk, hogy érvényesítse egy beérkezett adatcsere-vezérlőszám jelenlétét, és szükség esetén távolítsa el az entitást a Remove-AzIntegrationAccountReceivedIcn parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="c1fd5-107">Adja meg a "-AgreementType" paramétert annak megadásához, hogy az X12 vagy az Edifact típusú vezérlőszámok visszaadása</span><span class="sxs-lookup"><span data-stu-id="c1fd5-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c1fd5-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1fd5-108">EXAMPLES</span></span>

### <span data-ttu-id="c1fd5-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c1fd5-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="c1fd5-110">Ez a parancs az X12-es integrációs fiók átváltási vezérlőszámát kapja meg szerződésnév és vezérlőszámérték alapján.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="c1fd5-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="c1fd5-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="c1fd5-112">Ez a parancs az Edifact-integrációs fiókot szerződésnév és vezérlőszámérték alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="c1fd5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1fd5-113">PARAMETERS</span></span>

### <span data-ttu-id="c1fd5-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c1fd5-114">-AgreementName</span></span>
<span data-ttu-id="c1fd5-115">Az integrációs fiók szerződésének neve.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c1fd5-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="c1fd5-116">-AgreementType</span></span>
<span data-ttu-id="c1fd5-117">Az integrációs fiók szerződéstípusa.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="c1fd5-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="c1fd5-118">-ControlNumberValue</span></span>
<span data-ttu-id="c1fd5-119">Az integrációs fiók vezérlőszámának értéke.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="c1fd5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fd5-120">-DefaultProfile</span></span>
<span data-ttu-id="c1fd5-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c1fd5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1fd5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c1fd5-122">-Name</span></span>
<span data-ttu-id="c1fd5-123">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-123">The integration account name.</span></span>

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

### <span data-ttu-id="c1fd5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fd5-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1fd5-125">Az integrációs fiók erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c1fd5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fd5-126">CommonParameters</span></span>
<span data-ttu-id="c1fd5-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fd5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fd5-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fd5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fd5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1fd5-129">INPUTS</span></span>

### <span data-ttu-id="c1fd5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c1fd5-130">System.String</span></span>

## <span data-ttu-id="c1fd5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1fd5-131">OUTPUTS</span></span>

### <span data-ttu-id="c1fd5-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="c1fd5-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="c1fd5-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1fd5-133">NOTES</span></span>

## <span data-ttu-id="c1fd5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1fd5-134">RELATED LINKS</span></span>

[<span data-ttu-id="c1fd5-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c1fd5-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="c1fd5-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c1fd5-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
