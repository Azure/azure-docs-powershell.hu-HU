---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 4976c34437b2f858f8e76924754fe04a8b1e0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498564"
---
# <span data-ttu-id="06556-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="06556-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="06556-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06556-102">SYNOPSIS</span></span>
<span data-ttu-id="06556-103">Az Analysis Services-kiszolgáló példányainak törlése</span><span class="sxs-lookup"><span data-stu-id="06556-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06556-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06556-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06556-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06556-105">DESCRIPTION</span></span>
<span data-ttu-id="06556-106">Az Remove-AzureRmAnalysisServicesServer parancsmag törli az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="06556-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="06556-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06556-107">EXAMPLES</span></span>

### <span data-ttu-id="06556-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06556-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="06556-109">Ez a parancs eltávolítja a TestServer nevű kiszolgálót a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="06556-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="06556-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06556-110">PARAMETERS</span></span>

### <span data-ttu-id="06556-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06556-111">-DefaultProfile</span></span>
<span data-ttu-id="06556-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06556-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06556-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06556-113">-Name</span></span>
<span data-ttu-id="06556-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="06556-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06556-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06556-115">-PassThru</span></span>
<span data-ttu-id="06556-116">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="06556-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06556-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06556-117">-ResourceGroupName</span></span>
<span data-ttu-id="06556-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="06556-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06556-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06556-119">-Confirm</span></span>
<span data-ttu-id="06556-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="06556-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06556-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06556-121">-WhatIf</span></span>
<span data-ttu-id="06556-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="06556-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06556-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06556-123">CommonParameters</span></span>
<span data-ttu-id="06556-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06556-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06556-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06556-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06556-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06556-126">INPUTS</span></span>

### <span data-ttu-id="06556-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06556-127">System.String</span></span>

## <span data-ttu-id="06556-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06556-128">OUTPUTS</span></span>

### <span data-ttu-id="06556-129">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="06556-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="06556-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06556-130">NOTES</span></span>
<span data-ttu-id="06556-131">Alias: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="06556-131">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="06556-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06556-132">RELATED LINKS</span></span>

[<span data-ttu-id="06556-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="06556-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="06556-134">Új – AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="06556-134">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
