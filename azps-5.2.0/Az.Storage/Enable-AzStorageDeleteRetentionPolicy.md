---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349770"
---
# <span data-ttu-id="a62b0-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a62b0-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a62b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a62b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a62b0-103">Engedélyezze a törlési adatmegőrzési házirendet az Azure Storage Blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="a62b0-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="a62b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a62b0-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a62b0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a62b0-105">DESCRIPTION</span></span>
<span data-ttu-id="a62b0-106">Az **Enable-AzStorageDeleteRetentionPolicy parancsmag** törlési adatmegőrzési házirendet engedélyez az Azure Storage Blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="a62b0-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="a62b0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a62b0-107">EXAMPLES</span></span>

### <span data-ttu-id="a62b0-108">1. példa: A Blob szolgáltatás törlési adatmegőrzési házirendének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="a62b0-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="a62b0-109">Ezzel a paranccsal törlési adatmegőrzési házirendet állíthat be a Blob szolgáltatásban, a törölt blobmegőrzési napokat pedig 3-ra állíthatja.</span><span class="sxs-lookup"><span data-stu-id="a62b0-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="a62b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a62b0-110">PARAMETERS</span></span>

### <span data-ttu-id="a62b0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a62b0-111">-Context</span></span>
<span data-ttu-id="a62b0-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="a62b0-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a62b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62b0-113">-DefaultProfile</span></span>
<span data-ttu-id="a62b0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a62b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a62b0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a62b0-115">-PassThru</span></span>
<span data-ttu-id="a62b0-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="a62b0-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="a62b0-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="a62b0-117">-RetentionDays</span></span>
<span data-ttu-id="a62b0-118">Beállítja a DeleteRetentionPolicy adatmegőrzési napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="a62b0-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="a62b0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a62b0-119">-Confirm</span></span>
<span data-ttu-id="a62b0-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a62b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a62b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a62b0-121">-WhatIf</span></span>
<span data-ttu-id="a62b0-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a62b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a62b0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a62b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a62b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62b0-124">CommonParameters</span></span>
<span data-ttu-id="a62b0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62b0-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62b0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62b0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a62b0-127">INPUTS</span></span>

### <span data-ttu-id="a62b0-128">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a62b0-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a62b0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a62b0-129">OUTPUTS</span></span>

### <span data-ttu-id="a62b0-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a62b0-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a62b0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a62b0-131">NOTES</span></span>

## <span data-ttu-id="a62b0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a62b0-132">RELATED LINKS</span></span>
