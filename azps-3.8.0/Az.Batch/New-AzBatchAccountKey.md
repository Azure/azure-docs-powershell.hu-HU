---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: e079701f0d2ccca49e1368edc9446c08b4549c11
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017217"
---
# <span data-ttu-id="ab7bb-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ab7bb-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="ab7bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7bb-103">Újragenerálja a köteg-fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="ab7bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab7bb-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab7bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ab7bb-106">A **New-AzBatchAccountKey parancsmag újra** létrehoz egy Azure-köteg elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="ab7bb-107">A parancsmag egy **BatchAccountContext** objektumot ad eredményül, amely az aktuális **PrimaryAccountKey** és a **SecondaryAccountKey** tulajdonságaival rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="ab7bb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ab7bb-108">EXAMPLES</span></span>

### <span data-ttu-id="ab7bb-109">1. példa: az elsődleges fiók újragenerálása egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="ab7bb-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="ab7bb-110">Ez a parancs újragenerálja az elsődleges fiók kulcsot a pfuller nevű köteg számlán.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="ab7bb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab7bb-111">PARAMETERS</span></span>

### <span data-ttu-id="ab7bb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ab7bb-112">-AccountName</span></span>
<span data-ttu-id="ab7bb-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag létrehozta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ab7bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7bb-114">-DefaultProfile</span></span>
<span data-ttu-id="ab7bb-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab7bb-116">-Típus</span><span class="sxs-lookup"><span data-stu-id="ab7bb-116">-KeyType</span></span>
<span data-ttu-id="ab7bb-117">A parancsmag által újragenerált kulcs típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="ab7bb-118">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ab7bb-118">Valid values are:</span></span> 
- <span data-ttu-id="ab7bb-119">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="ab7bb-119">Primary</span></span>
- <span data-ttu-id="ab7bb-120">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="ab7bb-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab7bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab7bb-122">Annak a fióknak az erőforrás csoportját adja meg, amelyre a parancsmag létrehozta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ab7bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7bb-123">CommonParameters</span></span>
<span data-ttu-id="ab7bb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab7bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7bb-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ab7bb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7bb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab7bb-126">INPUTS</span></span>

### <span data-ttu-id="ab7bb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ab7bb-127">System.String</span></span>

## <span data-ttu-id="ab7bb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab7bb-128">OUTPUTS</span></span>

### <span data-ttu-id="ab7bb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab7bb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab7bb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab7bb-130">NOTES</span></span>

## <span data-ttu-id="ab7bb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab7bb-131">RELATED LINKS</span></span>

[<span data-ttu-id="ab7bb-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ab7bb-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ab7bb-133">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ab7bb-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


