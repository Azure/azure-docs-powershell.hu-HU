---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158130"
---
# <span data-ttu-id="40093-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="40093-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="40093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40093-102">SYNOPSIS</span></span>
<span data-ttu-id="40093-103">Szolgáltatástulajdonságokat kap az Azure Storage File Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="40093-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="40093-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40093-104">SYNTAX</span></span>

### <span data-ttu-id="40093-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40093-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40093-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="40093-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40093-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="40093-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40093-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40093-108">DESCRIPTION</span></span>
<span data-ttu-id="40093-109">A **Get-AzStorageFileServiceProperty** parancsmag az Azure Storage File Services szolgáltatástulajdonságokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="40093-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="40093-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40093-110">EXAMPLES</span></span>

### <span data-ttu-id="40093-111">1. példa: Azure Storage File Services tulajdonság lekérte egy adott tárfiókra</span><span class="sxs-lookup"><span data-stu-id="40093-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="40093-112">Ez a parancs egy adott tárfiók Fájlszolgáltatások tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="40093-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="40093-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40093-113">PARAMETERS</span></span>

### <span data-ttu-id="40093-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40093-114">-DefaultProfile</span></span>
<span data-ttu-id="40093-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40093-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40093-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40093-116">-ResourceGroupName</span></span>
<span data-ttu-id="40093-117">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40093-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="40093-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40093-118">-ResourceId</span></span>
<span data-ttu-id="40093-119">Adja meg a tárfiók erőforrás-azonosítóját vagy egy fájlszolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="40093-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="40093-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="40093-120">-StorageAccount</span></span>
<span data-ttu-id="40093-121">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="40093-121">Storage account object</span></span>

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

### <span data-ttu-id="40093-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40093-122">-StorageAccountName</span></span>
<span data-ttu-id="40093-123">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="40093-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="40093-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40093-124">CommonParameters</span></span>
<span data-ttu-id="40093-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40093-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40093-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40093-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40093-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40093-127">INPUTS</span></span>

### <span data-ttu-id="40093-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40093-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="40093-129">System.String</span><span class="sxs-lookup"><span data-stu-id="40093-129">System.String</span></span>

## <span data-ttu-id="40093-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40093-130">OUTPUTS</span></span>

### <span data-ttu-id="40093-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="40093-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="40093-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40093-132">NOTES</span></span>

## <span data-ttu-id="40093-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40093-133">RELATED LINKS</span></span>
