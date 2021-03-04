---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 9503f62667405c8e7a652bffc150a747eadb40f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933361"
---
# <span data-ttu-id="e9710-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e9710-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="e9710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9710-102">SYNOPSIS</span></span>
<span data-ttu-id="e9710-103">Szolgáltatástulajdonságokat kap az Azure Storage File Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e9710-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="e9710-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9710-104">SYNTAX</span></span>

### <span data-ttu-id="e9710-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9710-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9710-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e9710-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9710-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e9710-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9710-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9710-108">DESCRIPTION</span></span>
<span data-ttu-id="e9710-109">A **Get-AzStorageFileServiceProperty** parancsmag megkapja az Azure Storage File Services szolgáltatástulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e9710-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="e9710-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9710-110">EXAMPLES</span></span>

### <span data-ttu-id="e9710-111">1. példa: Azure Storage File Services tulajdonság lekérte egy adott tárfiókra</span><span class="sxs-lookup"><span data-stu-id="e9710-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 3
```

<span data-ttu-id="e9710-112">Ez a parancs egy adott tárfiók Fájlszolgáltatások tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9710-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="e9710-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9710-113">PARAMETERS</span></span>

### <span data-ttu-id="e9710-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9710-114">-DefaultProfile</span></span>
<span data-ttu-id="e9710-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9710-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9710-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9710-116">-ResourceGroupName</span></span>
<span data-ttu-id="e9710-117">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9710-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9710-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9710-118">-ResourceId</span></span>
<span data-ttu-id="e9710-119">Adja meg a tárfiók erőforrás-azonosítóját vagy egy fájlszolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e9710-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9710-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9710-120">-StorageAccount</span></span>
<span data-ttu-id="e9710-121">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="e9710-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9710-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e9710-122">-StorageAccountName</span></span>
<span data-ttu-id="e9710-123">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="e9710-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9710-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9710-124">CommonParameters</span></span>
<span data-ttu-id="e9710-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9710-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9710-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9710-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9710-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9710-127">INPUTS</span></span>

### <span data-ttu-id="e9710-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9710-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e9710-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9710-129">System.String</span></span>

## <span data-ttu-id="e9710-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9710-130">OUTPUTS</span></span>

### <span data-ttu-id="e9710-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="e9710-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="e9710-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9710-132">NOTES</span></span>

## <span data-ttu-id="e9710-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9710-133">RELATED LINKS</span></span>
