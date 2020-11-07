---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678999"
---
# <span data-ttu-id="a46cc-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a46cc-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="a46cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a46cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a46cc-103">Az Analysis Services Server egy példányának folytatása</span><span class="sxs-lookup"><span data-stu-id="a46cc-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a46cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a46cc-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a46cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a46cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a46cc-106">Az Resume-AzureRmAnalysisServicesServer parancsmag az Analysis Services Server egy példányát folytatja</span><span class="sxs-lookup"><span data-stu-id="a46cc-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="a46cc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a46cc-107">EXAMPLES</span></span>

### <span data-ttu-id="a46cc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a46cc-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="a46cc-109">Ez a parancs folytatja a TestServer nevű felfüggesztett kiszolgáló resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="a46cc-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="a46cc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a46cc-110">PARAMETERS</span></span>

### <span data-ttu-id="a46cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46cc-111">-DefaultProfile</span></span>
<span data-ttu-id="a46cc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a46cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a46cc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a46cc-113">-Name</span></span>
<span data-ttu-id="a46cc-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="a46cc-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46cc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a46cc-115">-PassThru</span></span>
<span data-ttu-id="a46cc-116">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="a46cc-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="a46cc-118">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="a46cc-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46cc-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a46cc-119">-Confirm</span></span>
<span data-ttu-id="a46cc-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="a46cc-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46cc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a46cc-121">-WhatIf</span></span>
<span data-ttu-id="a46cc-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="a46cc-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46cc-123">CommonParameters</span></span>
<span data-ttu-id="a46cc-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a46cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46cc-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46cc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46cc-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a46cc-126">INPUTS</span></span>

### <span data-ttu-id="a46cc-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="a46cc-127">None</span></span>
<span data-ttu-id="a46cc-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a46cc-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a46cc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a46cc-129">OUTPUTS</span></span>

### <span data-ttu-id="a46cc-130">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a46cc-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="a46cc-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a46cc-131">NOTES</span></span>
<span data-ttu-id="a46cc-132">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="a46cc-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="a46cc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a46cc-133">RELATED LINKS</span></span>

[<span data-ttu-id="a46cc-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a46cc-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="a46cc-135">Felfüggesztés – AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a46cc-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
