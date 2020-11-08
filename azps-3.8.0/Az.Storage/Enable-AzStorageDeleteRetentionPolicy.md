---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011251"
---
# <span data-ttu-id="7d459-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d459-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7d459-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d459-102">SYNOPSIS</span></span>
<span data-ttu-id="7d459-103">Engedélyezze az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="7d459-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7d459-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d459-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d459-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d459-105">DESCRIPTION</span></span>
<span data-ttu-id="7d459-106">Az **enable-AzStorageDeleteRetentionPolicy** parancsmag az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="7d459-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7d459-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d459-107">EXAMPLES</span></span>

### <span data-ttu-id="7d459-108">Példa 1: a blob-szolgáltatás adatmegőrzési házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="7d459-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="7d459-109">Ez a parancs engedélyezi a blob-szolgáltatás adatmegőrzési házirendjét, és a törölt blob-adatmegőrzési napokat a 3 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="7d459-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="7d459-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d459-110">PARAMETERS</span></span>

### <span data-ttu-id="7d459-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7d459-111">-Context</span></span>
<span data-ttu-id="7d459-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="7d459-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d459-113">-DefaultProfile</span></span>
<span data-ttu-id="7d459-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d459-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d459-115">-PassThru</span></span>
<span data-ttu-id="7d459-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="7d459-116">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="7d459-117">-RetentionDays</span></span>
<span data-ttu-id="7d459-118">Megadja a DeleteRetentionPolicy retenciós napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="7d459-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d459-119">-Confirm</span></span>
<span data-ttu-id="7d459-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d459-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d459-121">-WhatIf</span></span>
<span data-ttu-id="7d459-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d459-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d459-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d459-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d459-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d459-124">CommonParameters</span></span>
<span data-ttu-id="7d459-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d459-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d459-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d459-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d459-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d459-127">INPUTS</span></span>

### <span data-ttu-id="7d459-128">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d459-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7d459-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d459-129">OUTPUTS</span></span>

### <span data-ttu-id="7d459-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d459-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7d459-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d459-131">NOTES</span></span>

## <span data-ttu-id="7d459-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d459-132">RELATED LINKS</span></span>
