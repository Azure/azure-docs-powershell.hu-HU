---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502115"
---
# <span data-ttu-id="2514d-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="2514d-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="2514d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2514d-102">SYNOPSIS</span></span>
<span data-ttu-id="2514d-103">Létrehozza az Azure adatbázis-áttelepítési szolgáltatás fájlmegosztásról objektumát, amely a helyi hálózati megosztást adja meg a forrás adatbázis biztonsági másolatának elkészítéséhez.</span><span class="sxs-lookup"><span data-stu-id="2514d-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2514d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2514d-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2514d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2514d-105">DESCRIPTION</span></span>
<span data-ttu-id="2514d-106">A New-AzureRmDataMigrationFileShare parancsmag hozza létre a fájlmegosztásról objektumot, amely a helyi hálózati megosztást adja meg, amelyet az Azure adatbázis-áttelepítési szolgáltatás a forrás-adatbázis biztonsági másolatai készítéséhez használ</span><span class="sxs-lookup"><span data-stu-id="2514d-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="2514d-107">Az SQL Server-példányt futtató szolgáltatásfiók írási jogosultsággal kell rendelkeznie ebben a hálózati megosztásban.</span><span class="sxs-lookup"><span data-stu-id="2514d-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="2514d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2514d-108">EXAMPLES</span></span>

### <span data-ttu-id="2514d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2514d-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="2514d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2514d-110">PARAMETERS</span></span>

### <span data-ttu-id="2514d-111">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="2514d-111">-Credential</span></span>
<span data-ttu-id="2514d-112">Hitelesítő adatok a fájlmegosztás eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="2514d-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2514d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2514d-113">-DefaultProfile</span></span>
<span data-ttu-id="2514d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2514d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2514d-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="2514d-115">-Path</span></span>
<span data-ttu-id="2514d-116">Fájlmegosztási elérési út.</span><span class="sxs-lookup"><span data-stu-id="2514d-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2514d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2514d-117">CommonParameters</span></span>
<span data-ttu-id="2514d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2514d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2514d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2514d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2514d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2514d-120">INPUTS</span></span>

### <span data-ttu-id="2514d-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="2514d-121">None</span></span>

## <span data-ttu-id="2514d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2514d-122">OUTPUTS</span></span>

### <span data-ttu-id="2514d-123">Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="2514d-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="2514d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2514d-124">NOTES</span></span>

## <span data-ttu-id="2514d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2514d-125">RELATED LINKS</span></span>
