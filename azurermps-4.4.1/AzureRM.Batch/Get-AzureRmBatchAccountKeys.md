---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679792"
---
# <span data-ttu-id="e9dde-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e9dde-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="e9dde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9dde-102">SYNOPSIS</span></span>
<span data-ttu-id="e9dde-103">Egy köteg fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9dde-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9dde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9dde-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9dde-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9dde-105">DESCRIPTION</span></span>
<span data-ttu-id="e9dde-106">A **Get-AzureRmBatchAccountKeys** parancsmag az Azure-kötegek kulcsait az aktuális előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9dde-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="e9dde-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e9dde-107">EXAMPLES</span></span>

## <span data-ttu-id="e9dde-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9dde-108">PARAMETERS</span></span>

### <span data-ttu-id="e9dde-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9dde-109">-AccountName</span></span>
<span data-ttu-id="e9dde-110">Annak a fióknak a nevét adja meg, amelynek a parancsmagja kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="e9dde-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9dde-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9dde-111">-ResourceGroupName</span></span>
<span data-ttu-id="e9dde-112">Annak a fióknak a nevét adja meg az erőforráscsoport számára, amelynek a parancsmagja kulcsokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e9dde-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9dde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9dde-113">-DefaultProfile</span></span>
<span data-ttu-id="e9dde-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9dde-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9dde-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9dde-115">CommonParameters</span></span>
<span data-ttu-id="e9dde-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9dde-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9dde-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9dde-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9dde-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9dde-118">INPUTS</span></span>

## <span data-ttu-id="e9dde-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9dde-119">OUTPUTS</span></span>

### <span data-ttu-id="e9dde-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e9dde-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e9dde-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9dde-121">NOTES</span></span>

## <span data-ttu-id="e9dde-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9dde-122">RELATED LINKS</span></span>

[<span data-ttu-id="e9dde-123">Új – AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e9dde-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="e9dde-124">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e9dde-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


