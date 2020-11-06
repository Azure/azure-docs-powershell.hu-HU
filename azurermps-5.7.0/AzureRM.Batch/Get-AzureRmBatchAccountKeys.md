---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492394"
---
# <span data-ttu-id="d77f1-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d77f1-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="d77f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d77f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d77f1-103">Egy köteg fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d77f1-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d77f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d77f1-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d77f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d77f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d77f1-106">A **Get-AzureRmBatchAccountKeys** parancsmag az Azure-kötegek kulcsait az aktuális előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d77f1-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="d77f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d77f1-107">EXAMPLES</span></span>

## <span data-ttu-id="d77f1-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d77f1-108">PARAMETERS</span></span>

### <span data-ttu-id="d77f1-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d77f1-109">-AccountName</span></span>
<span data-ttu-id="d77f1-110">Annak a fióknak a nevét adja meg, amelynek a parancsmagja kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="d77f1-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d77f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77f1-111">-DefaultProfile</span></span>
<span data-ttu-id="d77f1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d77f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d77f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="d77f1-114">Annak a fióknak a nevét adja meg az erőforráscsoport számára, amelynek a parancsmagja kulcsokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d77f1-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d77f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77f1-115">CommonParameters</span></span>
<span data-ttu-id="d77f1-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d77f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77f1-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d77f1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77f1-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d77f1-118">INPUTS</span></span>

### <span data-ttu-id="d77f1-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="d77f1-119">None</span></span>
<span data-ttu-id="d77f1-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d77f1-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d77f1-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d77f1-121">OUTPUTS</span></span>

### <span data-ttu-id="d77f1-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d77f1-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d77f1-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d77f1-123">NOTES</span></span>

## <span data-ttu-id="d77f1-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d77f1-124">RELATED LINKS</span></span>

[<span data-ttu-id="d77f1-125">Új – AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d77f1-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="d77f1-126">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d77f1-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


