---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 1f32e700cd5d0c20e041143e43755172ecf2da86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502227"
---
# <span data-ttu-id="10bf5-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="10bf5-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="10bf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="10bf5-103">Egy köteg fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="10bf5-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10bf5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10bf5-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10bf5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="10bf5-106">A **Get-AzureRmBatchAccountKeys** parancsmag az Azure-kötegek kulcsait az aktuális előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="10bf5-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="10bf5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10bf5-107">EXAMPLES</span></span>

## <span data-ttu-id="10bf5-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10bf5-108">PARAMETERS</span></span>

### <span data-ttu-id="10bf5-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10bf5-109">-AccountName</span></span>
<span data-ttu-id="10bf5-110">Annak a fióknak a nevét adja meg, amelynek a parancsmagja kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="10bf5-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="10bf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bf5-111">-DefaultProfile</span></span>
<span data-ttu-id="10bf5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10bf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10bf5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bf5-113">-ResourceGroupName</span></span>
<span data-ttu-id="10bf5-114">Annak a fióknak a nevét adja meg az erőforráscsoport számára, amelynek a parancsmagja kulcsokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="10bf5-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="10bf5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bf5-115">CommonParameters</span></span>
<span data-ttu-id="10bf5-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10bf5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bf5-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10bf5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bf5-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10bf5-118">INPUTS</span></span>

### <span data-ttu-id="10bf5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="10bf5-119">System.String</span></span>

## <span data-ttu-id="10bf5-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10bf5-120">OUTPUTS</span></span>

### <span data-ttu-id="10bf5-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="10bf5-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="10bf5-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10bf5-122">NOTES</span></span>

## <span data-ttu-id="10bf5-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10bf5-123">RELATED LINKS</span></span>

[<span data-ttu-id="10bf5-124">Új – AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="10bf5-124">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="10bf5-125">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="10bf5-125">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


