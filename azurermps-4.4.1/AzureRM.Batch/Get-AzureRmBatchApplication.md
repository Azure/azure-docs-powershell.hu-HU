---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: b8169b2f05b4272c92989768e672b30aee105f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502768"
---
# <span data-ttu-id="d5e84-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d5e84-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="d5e84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5e84-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e84-103">Információt kap a megadott alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="d5e84-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5e84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5e84-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5e84-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e84-106">A **Get-AzureRmBatchApplication** parancsmag az Azure-alapú köteg-fiókokban található alkalmazásokkal kapcsolatos információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e84-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="d5e84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d5e84-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e84-108">Példa 1: az alkalmazások megjelenítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="d5e84-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="d5e84-109">Ez a parancs megjeleníti az ContosoBatch-fiók összes alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="d5e84-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="d5e84-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5e84-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e84-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5e84-111">-AccountName</span></span>
<span data-ttu-id="d5e84-112">Az alkalmazást tartalmazó köteg fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e84-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="d5e84-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d5e84-113">-ApplicationId</span></span>
<span data-ttu-id="d5e84-114">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e84-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e84-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e84-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5e84-116">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5e84-116">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e84-117">-DefaultProfile</span></span>
<span data-ttu-id="d5e84-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5e84-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e84-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e84-119">CommonParameters</span></span>
<span data-ttu-id="d5e84-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5e84-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e84-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e84-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e84-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5e84-122">INPUTS</span></span>

## <span data-ttu-id="d5e84-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5e84-123">OUTPUTS</span></span>

### <span data-ttu-id="d5e84-124">Microsoft.Azure.Commands.BatCH. Modellek. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d5e84-124">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="d5e84-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5e84-125">NOTES</span></span>

## <span data-ttu-id="d5e84-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5e84-126">RELATED LINKS</span></span>

[<span data-ttu-id="d5e84-127">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d5e84-127">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d5e84-128">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d5e84-128">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="d5e84-129">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d5e84-129">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d5e84-130">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d5e84-130">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d5e84-131">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d5e84-131">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d5e84-132">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d5e84-132">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


