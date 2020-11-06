---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: df7229668547e1c018067effe50e823354d64736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504588"
---
# <span data-ttu-id="b6496-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b6496-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="b6496-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6496-102">SYNOPSIS</span></span>
<span data-ttu-id="b6496-103">Egy alkalmazást töröl egy köteg fiókból.</span><span class="sxs-lookup"><span data-stu-id="b6496-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6496-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6496-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6496-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6496-105">DESCRIPTION</span></span>
<span data-ttu-id="b6496-106">A **Remove-AzureRmBatchApplication** parancsmag egy alkalmazást egy Azure-kötegbeli fiókból töröl.</span><span class="sxs-lookup"><span data-stu-id="b6496-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="b6496-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6496-107">EXAMPLES</span></span>

### <span data-ttu-id="b6496-108">Példa 1: alkalmazás törlése egy köteg fiókból</span><span class="sxs-lookup"><span data-stu-id="b6496-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="b6496-109">Ez a parancs törli a Bárdos Iparcikk alkalmazást az ContosoBatch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="b6496-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="b6496-110">A parancs nem működik, ha az alkalmazás bármely csomagot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b6496-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="b6496-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6496-111">PARAMETERS</span></span>

### <span data-ttu-id="b6496-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6496-112">-AccountName</span></span>
<span data-ttu-id="b6496-113">Annak a kötegelt fióknak a neve, amelyből a parancsmag eltávolítja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b6496-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="b6496-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b6496-114">-ApplicationId</span></span>
<span data-ttu-id="b6496-115">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6496-115">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6496-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6496-116">-DefaultProfile</span></span>
<span data-ttu-id="b6496-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6496-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6496-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6496-118">-ResourceGroupName</span></span>
<span data-ttu-id="b6496-119">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6496-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b6496-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6496-120">CommonParameters</span></span>
<span data-ttu-id="b6496-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6496-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6496-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6496-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6496-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6496-123">INPUTS</span></span>

### <span data-ttu-id="b6496-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="b6496-124">None</span></span>
<span data-ttu-id="b6496-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b6496-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6496-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6496-126">OUTPUTS</span></span>

## <span data-ttu-id="b6496-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6496-127">NOTES</span></span>

## <span data-ttu-id="b6496-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6496-128">RELATED LINKS</span></span>

[<span data-ttu-id="b6496-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b6496-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="b6496-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b6496-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b6496-131">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b6496-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="b6496-132">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b6496-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b6496-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b6496-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b6496-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b6496-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


