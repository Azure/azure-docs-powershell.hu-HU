---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187657"
---
# <span data-ttu-id="8faa0-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8faa0-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="8faa0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8faa0-102">SYNOPSIS</span></span>
<span data-ttu-id="8faa0-103">Újragenerálja a köteg-fiók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="8faa0-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="8faa0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8faa0-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8faa0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8faa0-105">DESCRIPTION</span></span>
<span data-ttu-id="8faa0-106">A **New-AzBatchAccountKey parancsmag újra** létrehoz egy Azure-köteg elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="8faa0-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="8faa0-107">A parancsmag egy **BatchAccountContext** objektumot ad eredményül, amely az aktuális **PrimaryAccountKey** és a **SecondaryAccountKey** tulajdonságaival rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="8faa0-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="8faa0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8faa0-108">EXAMPLES</span></span>

### <span data-ttu-id="8faa0-109">1. példa: az elsődleges fiók újragenerálása egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="8faa0-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="8faa0-110">Ez a parancs újragenerálja az elsődleges fiók kulcsot a pfuller nevű köteg számlán.</span><span class="sxs-lookup"><span data-stu-id="8faa0-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="8faa0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8faa0-111">PARAMETERS</span></span>

### <span data-ttu-id="8faa0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8faa0-112">-AccountName</span></span>
<span data-ttu-id="8faa0-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag létrehozta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8faa0-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="8faa0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8faa0-114">-DefaultProfile</span></span>
<span data-ttu-id="8faa0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8faa0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8faa0-116">-Típus</span><span class="sxs-lookup"><span data-stu-id="8faa0-116">-KeyType</span></span>
<span data-ttu-id="8faa0-117">A parancsmag által újragenerált kulcs típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="8faa0-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="8faa0-118">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8faa0-118">Valid values are:</span></span>
- <span data-ttu-id="8faa0-119">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="8faa0-119">Primary</span></span>
- <span data-ttu-id="8faa0-120">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="8faa0-120">Secondary</span></span>

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

### <span data-ttu-id="8faa0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8faa0-121">-ResourceGroupName</span></span>
<span data-ttu-id="8faa0-122">Annak a fióknak az erőforrás csoportját adja meg, amelyre a parancsmag létrehozta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8faa0-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="8faa0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8faa0-123">CommonParameters</span></span>
<span data-ttu-id="8faa0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8faa0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8faa0-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8faa0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8faa0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8faa0-126">INPUTS</span></span>

### <span data-ttu-id="8faa0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8faa0-127">System.String</span></span>

## <span data-ttu-id="8faa0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8faa0-128">OUTPUTS</span></span>

### <span data-ttu-id="8faa0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8faa0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8faa0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8faa0-130">NOTES</span></span>

## <span data-ttu-id="8faa0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8faa0-131">RELATED LINKS</span></span>

[<span data-ttu-id="8faa0-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8faa0-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8faa0-133">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8faa0-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
