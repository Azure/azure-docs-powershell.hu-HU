---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 067f3be3aa668ba5402881b697d7def09cb88658
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503099"
---
# <span data-ttu-id="23fdd-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="23fdd-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="23fdd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="23fdd-103">Újragenerálja a köteg-fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="23fdd-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23fdd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23fdd-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23fdd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="23fdd-106">A **New-AzureRmBatchAccountKey parancsmag újra** létrehoz egy Azure-köteg elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="23fdd-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="23fdd-107">A parancsmag egy **BatchAccountContext** objektumot ad eredményül, amely az aktuális **PrimaryAccountKey** és a **SecondaryAccountKey** tulajdonságaival rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="23fdd-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="23fdd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="23fdd-108">EXAMPLES</span></span>

### <span data-ttu-id="23fdd-109">1. példa: az elsődleges fiók újragenerálása egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="23fdd-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="23fdd-110">Ez a parancs újragenerálja az elsődleges fiók kulcsot a pfuller nevű köteg számlán.</span><span class="sxs-lookup"><span data-stu-id="23fdd-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="23fdd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23fdd-111">PARAMETERS</span></span>

### <span data-ttu-id="23fdd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23fdd-112">-AccountName</span></span>
<span data-ttu-id="23fdd-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag létrehozta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="23fdd-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="23fdd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fdd-114">-DefaultProfile</span></span>
<span data-ttu-id="23fdd-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23fdd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23fdd-116">-Típus</span><span class="sxs-lookup"><span data-stu-id="23fdd-116">-KeyType</span></span>
<span data-ttu-id="23fdd-117">A parancsmag által újragenerált kulcs típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="23fdd-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="23fdd-118">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="23fdd-118">Valid values are:</span></span> 

- <span data-ttu-id="23fdd-119">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="23fdd-119">Primary</span></span>
- <span data-ttu-id="23fdd-120">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="23fdd-120">Secondary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fdd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23fdd-121">-ResourceGroupName</span></span>
<span data-ttu-id="23fdd-122">Annak a fióknak az erőforrás csoportját adja meg, amelyre a parancsmag létrehozta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="23fdd-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="23fdd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fdd-123">CommonParameters</span></span>
<span data-ttu-id="23fdd-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23fdd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fdd-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fdd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fdd-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23fdd-126">INPUTS</span></span>

### <span data-ttu-id="23fdd-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="23fdd-127">None</span></span>
<span data-ttu-id="23fdd-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="23fdd-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23fdd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23fdd-129">OUTPUTS</span></span>

### <span data-ttu-id="23fdd-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23fdd-130">BatchAccountContext</span></span>

## <span data-ttu-id="23fdd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23fdd-131">NOTES</span></span>

## <span data-ttu-id="23fdd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23fdd-132">RELATED LINKS</span></span>

[<span data-ttu-id="23fdd-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="23fdd-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="23fdd-134">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="23fdd-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

