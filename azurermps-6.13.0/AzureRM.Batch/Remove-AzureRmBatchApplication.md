---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 61288340bb2b9acb2bd47388d8f776d5c732b6f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492864"
---
# <span data-ttu-id="64761-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64761-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="64761-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64761-102">SYNOPSIS</span></span>
<span data-ttu-id="64761-103">Egy alkalmazást töröl egy köteg fiókból.</span><span class="sxs-lookup"><span data-stu-id="64761-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64761-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64761-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64761-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64761-105">DESCRIPTION</span></span>
<span data-ttu-id="64761-106">A **Remove-AzureRmBatchApplication** parancsmag egy alkalmazást egy Azure-kötegbeli fiókból töröl.</span><span class="sxs-lookup"><span data-stu-id="64761-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="64761-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64761-107">EXAMPLES</span></span>

### <span data-ttu-id="64761-108">Példa 1: alkalmazás törlése egy köteg fiókból</span><span class="sxs-lookup"><span data-stu-id="64761-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="64761-109">Ez a parancs törli a Bárdos Iparcikk alkalmazást az ContosoBatch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="64761-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="64761-110">A parancs nem működik, ha az alkalmazás bármely csomagot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="64761-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="64761-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64761-111">PARAMETERS</span></span>

### <span data-ttu-id="64761-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64761-112">-AccountName</span></span>
<span data-ttu-id="64761-113">Annak a kötegelt fióknak a neve, amelyből a parancsmag eltávolítja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="64761-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="64761-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="64761-114">-ApplicationId</span></span>
<span data-ttu-id="64761-115">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64761-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64761-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64761-116">-DefaultProfile</span></span>
<span data-ttu-id="64761-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64761-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64761-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64761-118">-ResourceGroupName</span></span>
<span data-ttu-id="64761-119">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64761-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="64761-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64761-120">CommonParameters</span></span>
<span data-ttu-id="64761-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64761-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64761-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64761-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64761-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64761-123">INPUTS</span></span>

### <span data-ttu-id="64761-124">System. String</span><span class="sxs-lookup"><span data-stu-id="64761-124">System.String</span></span>

## <span data-ttu-id="64761-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64761-125">OUTPUTS</span></span>

### <span data-ttu-id="64761-126">System. Void</span><span class="sxs-lookup"><span data-stu-id="64761-126">System.Void</span></span>

## <span data-ttu-id="64761-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64761-127">NOTES</span></span>

## <span data-ttu-id="64761-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64761-128">RELATED LINKS</span></span>

[<span data-ttu-id="64761-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64761-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="64761-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="64761-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="64761-131">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64761-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="64761-132">Új – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="64761-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="64761-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="64761-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="64761-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64761-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


