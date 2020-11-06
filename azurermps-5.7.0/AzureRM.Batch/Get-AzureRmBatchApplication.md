---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: e22d3c58072fbabd3f927f6b9065f22422492622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492392"
---
# <span data-ttu-id="ef383-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ef383-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="ef383-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef383-102">SYNOPSIS</span></span>
<span data-ttu-id="ef383-103">Információt kap a megadott alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="ef383-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef383-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef383-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef383-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef383-105">DESCRIPTION</span></span>
<span data-ttu-id="ef383-106">A **Get-AzureRmBatchApplication** parancsmag az Azure-alapú köteg-fiókokban található alkalmazásokkal kapcsolatos információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ef383-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="ef383-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef383-107">EXAMPLES</span></span>

### <span data-ttu-id="ef383-108">Példa 1: az alkalmazások megjelenítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="ef383-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="ef383-109">Ez a parancs megjeleníti az ContosoBatch-fiók összes alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="ef383-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="ef383-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef383-110">PARAMETERS</span></span>

### <span data-ttu-id="ef383-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef383-111">-AccountName</span></span>
<span data-ttu-id="ef383-112">Az alkalmazást tartalmazó köteg fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef383-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="ef383-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ef383-113">-ApplicationId</span></span>
<span data-ttu-id="ef383-114">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef383-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef383-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef383-115">-DefaultProfile</span></span>
<span data-ttu-id="ef383-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef383-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef383-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef383-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef383-118">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef383-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef383-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef383-119">CommonParameters</span></span>
<span data-ttu-id="ef383-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef383-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef383-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef383-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef383-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef383-122">INPUTS</span></span>

### <span data-ttu-id="ef383-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef383-123">None</span></span>
<span data-ttu-id="ef383-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ef383-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef383-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef383-125">OUTPUTS</span></span>

### <span data-ttu-id="ef383-126">Microsoft.Azure.Commands.BatCH. Modellek. PSApplication</span><span class="sxs-lookup"><span data-stu-id="ef383-126">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="ef383-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef383-127">NOTES</span></span>

## <span data-ttu-id="ef383-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef383-128">RELATED LINKS</span></span>

[<span data-ttu-id="ef383-129">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ef383-129">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ef383-130">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ef383-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="ef383-131">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ef383-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ef383-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ef383-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="ef383-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ef383-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ef383-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ef383-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


