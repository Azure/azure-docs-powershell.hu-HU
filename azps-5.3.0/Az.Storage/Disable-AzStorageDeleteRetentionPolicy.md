---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374148"
---
# <span data-ttu-id="5a963-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a963-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="5a963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a963-102">SYNOPSIS</span></span>
<span data-ttu-id="5a963-103">Tiltsa le az Azure Storage Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="5a963-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="5a963-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a963-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a963-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a963-105">DESCRIPTION</span></span>
<span data-ttu-id="5a963-106">A **Disable-AzStorageDeleteRetentionPolicy** parancsmag letiltja az Azure Storage Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="5a963-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="5a963-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a963-107">EXAMPLES</span></span>

### <span data-ttu-id="5a963-108">1. példa: A Blob szolgáltatás törlési adatmegőrzési házirendének letiltása</span><span class="sxs-lookup"><span data-stu-id="5a963-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="5a963-109">Ez a parancs letiltja a Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="5a963-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="5a963-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a963-110">PARAMETERS</span></span>

### <span data-ttu-id="5a963-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5a963-111">-Context</span></span>
<span data-ttu-id="5a963-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="5a963-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="5a963-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a963-113">-DefaultProfile</span></span>
<span data-ttu-id="5a963-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a963-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a963-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a963-115">-PassThru</span></span>
<span data-ttu-id="5a963-116">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="5a963-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="5a963-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a963-117">-Confirm</span></span>
<span data-ttu-id="5a963-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a963-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a963-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a963-119">-WhatIf</span></span>
<span data-ttu-id="5a963-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a963-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a963-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a963-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a963-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a963-122">CommonParameters</span></span>
<span data-ttu-id="5a963-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a963-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a963-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a963-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a963-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a963-125">INPUTS</span></span>

### <span data-ttu-id="5a963-126">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a963-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5a963-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a963-127">OUTPUTS</span></span>

### <span data-ttu-id="5a963-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a963-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="5a963-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a963-129">NOTES</span></span>

## <span data-ttu-id="5a963-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a963-130">RELATED LINKS</span></span>
