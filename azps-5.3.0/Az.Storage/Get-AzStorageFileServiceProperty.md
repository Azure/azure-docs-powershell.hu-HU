---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479473"
---
# <span data-ttu-id="d5298-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d5298-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="d5298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5298-102">SYNOPSIS</span></span>
<span data-ttu-id="d5298-103">Szolgáltatástulajdonságokat kap az Azure Storage File Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="d5298-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="d5298-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5298-104">SYNTAX</span></span>

### <span data-ttu-id="d5298-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5298-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5298-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d5298-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5298-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d5298-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5298-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5298-108">DESCRIPTION</span></span>
<span data-ttu-id="d5298-109">A **Get-AzStorageFileServiceProperty** parancsmag megkapja az Azure Storage File Services szolgáltatástulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d5298-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="d5298-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5298-110">EXAMPLES</span></span>

### <span data-ttu-id="d5298-111">1. példa: Azure Storage File Services tulajdonság lekérte egy adott tárfiókra</span><span class="sxs-lookup"><span data-stu-id="d5298-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="d5298-112">Ez a parancs egy adott tárfiók Fájlszolgáltatások tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5298-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="d5298-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5298-113">PARAMETERS</span></span>

### <span data-ttu-id="d5298-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5298-114">-DefaultProfile</span></span>
<span data-ttu-id="d5298-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5298-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5298-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5298-116">-ResourceGroupName</span></span>
<span data-ttu-id="d5298-117">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5298-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5298-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5298-118">-ResourceId</span></span>
<span data-ttu-id="d5298-119">Adja meg a tárfiók erőforrás-azonosítóját vagy egy fájlszolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="d5298-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="d5298-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5298-120">-StorageAccount</span></span>
<span data-ttu-id="d5298-121">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="d5298-121">Storage account object</span></span>

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

### <span data-ttu-id="d5298-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5298-122">-StorageAccountName</span></span>
<span data-ttu-id="d5298-123">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="d5298-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="d5298-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5298-124">CommonParameters</span></span>
<span data-ttu-id="d5298-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5298-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5298-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5298-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5298-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5298-127">INPUTS</span></span>

### <span data-ttu-id="d5298-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5298-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d5298-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5298-129">System.String</span></span>

## <span data-ttu-id="d5298-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5298-130">OUTPUTS</span></span>

### <span data-ttu-id="d5298-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d5298-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="d5298-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5298-132">NOTES</span></span>

## <span data-ttu-id="d5298-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5298-133">RELATED LINKS</span></span>
