---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: fa08214e141d035e7c449e591f6a4820f758b48c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671473"
---
# <span data-ttu-id="ea023-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ea023-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="ea023-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea023-102">SYNOPSIS</span></span>
<span data-ttu-id="ea023-103">Információt kap a megadott alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="ea023-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="ea023-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea023-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea023-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea023-105">DESCRIPTION</span></span>
<span data-ttu-id="ea023-106">A **Get-AzBatchApplication** parancsmag az Azure-alapú köteg-fiókokban található alkalmazásokkal kapcsolatos információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ea023-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="ea023-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ea023-107">EXAMPLES</span></span>

### <span data-ttu-id="ea023-108">Példa 1: az alkalmazások megjelenítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="ea023-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="ea023-109">Ez a parancs megjeleníti az ContosoBatch-fiók összes alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="ea023-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="ea023-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea023-110">PARAMETERS</span></span>

### <span data-ttu-id="ea023-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea023-111">-AccountName</span></span>
<span data-ttu-id="ea023-112">Az alkalmazást tartalmazó köteg fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea023-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="ea023-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ea023-113">-ApplicationId</span></span>
<span data-ttu-id="ea023-114">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea023-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="ea023-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea023-115">-DefaultProfile</span></span>
<span data-ttu-id="ea023-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea023-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea023-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea023-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea023-118">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea023-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ea023-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea023-119">CommonParameters</span></span>
<span data-ttu-id="ea023-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea023-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea023-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea023-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea023-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea023-122">INPUTS</span></span>

### <span data-ttu-id="ea023-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ea023-123">System.String</span></span>

## <span data-ttu-id="ea023-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea023-124">OUTPUTS</span></span>

### <span data-ttu-id="ea023-125">Microsoft.Azure.Commands.BatCH. Modellek. PSApplication</span><span class="sxs-lookup"><span data-stu-id="ea023-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="ea023-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea023-126">NOTES</span></span>

## <span data-ttu-id="ea023-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea023-127">RELATED LINKS</span></span>

[<span data-ttu-id="ea023-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ea023-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="ea023-129">Új – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ea023-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="ea023-130">Új – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ea023-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="ea023-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ea023-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="ea023-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ea023-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="ea023-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ea023-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


