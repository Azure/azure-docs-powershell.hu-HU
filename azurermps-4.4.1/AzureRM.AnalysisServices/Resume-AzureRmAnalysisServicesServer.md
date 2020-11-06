---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492631"
---
# <span data-ttu-id="3e573-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3e573-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="3e573-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e573-102">SYNOPSIS</span></span>
<span data-ttu-id="3e573-103">Az Analysis Services Server egy példányának folytatása</span><span class="sxs-lookup"><span data-stu-id="3e573-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e573-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e573-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e573-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e573-105">DESCRIPTION</span></span>
<span data-ttu-id="3e573-106">Az Resume-AzureRmAnalysisServicesServer parancsmag az Analysis Services Server egy példányát folytatja</span><span class="sxs-lookup"><span data-stu-id="3e573-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="3e573-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e573-107">EXAMPLES</span></span>

### <span data-ttu-id="3e573-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3e573-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="3e573-109">Ez a parancs folytatja a TestServer nevű felfüggesztett kiszolgáló resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="3e573-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="3e573-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e573-110">PARAMETERS</span></span>

### <span data-ttu-id="3e573-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e573-111">-Name</span></span>
<span data-ttu-id="3e573-112">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="3e573-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="3e573-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e573-113">-PassThru</span></span>
<span data-ttu-id="3e573-114">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="3e573-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="3e573-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e573-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e573-116">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="3e573-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="3e573-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e573-117">-Confirm</span></span>
<span data-ttu-id="3e573-118">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="3e573-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3e573-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e573-119">-WhatIf</span></span>
<span data-ttu-id="3e573-120">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="3e573-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3e573-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e573-121">CommonParameters</span></span>
<span data-ttu-id="3e573-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e573-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e573-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e573-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e573-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e573-124">INPUTS</span></span>

## <span data-ttu-id="3e573-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e573-125">OUTPUTS</span></span>

### <span data-ttu-id="3e573-126">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3e573-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="3e573-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e573-127">NOTES</span></span>
<span data-ttu-id="3e573-128">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="3e573-128">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="3e573-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e573-129">RELATED LINKS</span></span>

[<span data-ttu-id="3e573-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3e573-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="3e573-131">Felfüggesztés – AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3e573-131">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
