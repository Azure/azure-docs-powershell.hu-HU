---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187078"
---
# <span data-ttu-id="e26a3-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e26a3-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="e26a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e26a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e26a3-103">Egy alkalmazást töröl egy köteg fiókból.</span><span class="sxs-lookup"><span data-stu-id="e26a3-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="e26a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e26a3-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e26a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e26a3-106">A **Remove-AzBatchApplication** parancsmag egy alkalmazást egy Azure-kötegbeli fiókból töröl.</span><span class="sxs-lookup"><span data-stu-id="e26a3-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="e26a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e26a3-107">EXAMPLES</span></span>

### <span data-ttu-id="e26a3-108">Példa 1: alkalmazás törlése egy köteg fiókból</span><span class="sxs-lookup"><span data-stu-id="e26a3-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="e26a3-109">Ez a parancs törli a Bárdos Iparcikk alkalmazást az ContosoBatch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="e26a3-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="e26a3-110">A parancs nem működik, ha az alkalmazás bármely csomagot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e26a3-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="e26a3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e26a3-111">PARAMETERS</span></span>

### <span data-ttu-id="e26a3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e26a3-112">-AccountName</span></span>
<span data-ttu-id="e26a3-113">Annak a kötegelt fióknak a neve, amelyből a parancsmag eltávolítja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="e26a3-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="e26a3-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e26a3-114">-ApplicationName</span></span>
<span data-ttu-id="e26a3-115">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e26a3-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e26a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26a3-116">-DefaultProfile</span></span>
<span data-ttu-id="e26a3-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e26a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e26a3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e26a3-118">-ResourceGroupName</span></span>
<span data-ttu-id="e26a3-119">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e26a3-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="e26a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26a3-120">CommonParameters</span></span>
<span data-ttu-id="e26a3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e26a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26a3-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e26a3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26a3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e26a3-123">INPUTS</span></span>

### <span data-ttu-id="e26a3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e26a3-124">System.String</span></span>

## <span data-ttu-id="e26a3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e26a3-125">OUTPUTS</span></span>

### <span data-ttu-id="e26a3-126">System. Void</span><span class="sxs-lookup"><span data-stu-id="e26a3-126">System.Void</span></span>

## <span data-ttu-id="e26a3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e26a3-127">NOTES</span></span>

## <span data-ttu-id="e26a3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e26a3-128">RELATED LINKS</span></span>

[<span data-ttu-id="e26a3-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e26a3-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="e26a3-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e26a3-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="e26a3-131">Új – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e26a3-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e26a3-132">Új – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e26a3-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="e26a3-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e26a3-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="e26a3-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e26a3-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


