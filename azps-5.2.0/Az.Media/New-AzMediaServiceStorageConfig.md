---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: d53edc73bb1813841403348919758f1c6c13eff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341801"
---
# <span data-ttu-id="034aa-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="034aa-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="034aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034aa-102">SYNOPSIS</span></span>
<span data-ttu-id="034aa-103">Hozzon létre tárfiók-konfigurációt a médiaszolgáltatás-parancsmagok számára.</span><span class="sxs-lookup"><span data-stu-id="034aa-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="034aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="034aa-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="034aa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="034aa-105">DESCRIPTION</span></span>
<span data-ttu-id="034aa-106">A **New-AzMediaServiceStorageConfig** parancsmag létrehoz egy tárfiók-konfigurációt a médiaszolgáltatás-parancsmagok számára.</span><span class="sxs-lookup"><span data-stu-id="034aa-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="034aa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="034aa-107">EXAMPLES</span></span>

### <span data-ttu-id="034aa-108">1. példa: Tárfiók-konfiguráció létrehozása a médiaszolgáltatás-parancsmagok számára</span><span class="sxs-lookup"><span data-stu-id="034aa-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="034aa-109">Az első parancs egy tárfiók-objektumot hoz létre a **New-AzStorageAccount** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="034aa-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="034aa-110">A tárfiók neve Tár1, a típus neve pedig Standard_GRS az eredményt a $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="034aa-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="034aa-111">A második parancs egy tárolási konfigurációs objektumot hoz létre a médiaszolgáltatáshoz társított elsődleges tárfiókként a $StorageAccount tárolt tárfiók-azonosító adataival.</span><span class="sxs-lookup"><span data-stu-id="034aa-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="034aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="034aa-112">PARAMETERS</span></span>

### <span data-ttu-id="034aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034aa-113">-DefaultProfile</span></span>
<span data-ttu-id="034aa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="034aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="034aa-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="034aa-115">-IsPrimary</span></span>
<span data-ttu-id="034aa-116">Azt jelzi, hogy a parancsmag a médiaszolgáltatás elsődleges tárhelyeként hozza létre a tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="034aa-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034aa-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="034aa-117">-StorageAccountId</span></span>
<span data-ttu-id="034aa-118">A tárfiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="034aa-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="034aa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="034aa-119">-Confirm</span></span>
<span data-ttu-id="034aa-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="034aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034aa-121">-WhatIf</span></span>
<span data-ttu-id="034aa-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="034aa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034aa-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="034aa-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034aa-124">CommonParameters</span></span>
<span data-ttu-id="034aa-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034aa-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034aa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034aa-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="034aa-127">INPUTS</span></span>

### <span data-ttu-id="034aa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="034aa-128">System.String</span></span>

## <span data-ttu-id="034aa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="034aa-129">OUTPUTS</span></span>

### <span data-ttu-id="034aa-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="034aa-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="034aa-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="034aa-131">NOTES</span></span>

## <span data-ttu-id="034aa-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="034aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="034aa-133">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="034aa-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)


