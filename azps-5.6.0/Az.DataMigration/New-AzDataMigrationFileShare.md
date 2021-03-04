---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: b30f9fd4b29a1be064a9e0925e39faa71485b58f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925905"
---
# <span data-ttu-id="1b153-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="1b153-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="1b153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b153-102">SYNOPSIS</span></span>
<span data-ttu-id="1b153-103">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás FileShare objektumát, amely megadja a helyi hálózati megosztást, amelybe a forrásadatbázis biztonsági másolatát át kell vinni.</span><span class="sxs-lookup"><span data-stu-id="1b153-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="1b153-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b153-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b153-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b153-105">DESCRIPTION</span></span>
<span data-ttu-id="1b153-106">Az New-AzDataMigrationFileShare parancsmag létrehozza a FileShare objektumot, amely megadja azt a helyi hálózati megosztást, amelybe az Azure Database Migration Service forrásadatbázis-biztonsági másolatot tud készíteni.</span><span class="sxs-lookup"><span data-stu-id="1b153-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="1b153-107">A forrás SQL Server-példányt futtató szolgáltatásfióknak írási jogosultsággal kell rendelkezik a hálózati megosztáson.</span><span class="sxs-lookup"><span data-stu-id="1b153-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="1b153-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b153-108">EXAMPLES</span></span>

### <span data-ttu-id="1b153-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="1b153-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="1b153-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b153-110">PARAMETERS</span></span>

### <span data-ttu-id="1b153-111">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="1b153-111">-Credential</span></span>
<span data-ttu-id="1b153-112">Hitelesítő adatok a fájlmegosztás eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="1b153-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="1b153-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b153-113">-DefaultProfile</span></span>
<span data-ttu-id="1b153-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b153-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b153-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1b153-115">-Path</span></span>
<span data-ttu-id="1b153-116">Fájlmegosztási útvonal.</span><span class="sxs-lookup"><span data-stu-id="1b153-116">File share path.</span></span>

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

### <span data-ttu-id="1b153-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b153-117">CommonParameters</span></span>
<span data-ttu-id="1b153-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b153-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b153-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b153-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b153-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b153-120">INPUTS</span></span>

### <span data-ttu-id="1b153-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="1b153-121">None</span></span>

## <span data-ttu-id="1b153-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b153-122">OUTPUTS</span></span>

### <span data-ttu-id="1b153-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="1b153-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="1b153-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b153-124">NOTES</span></span>

## <span data-ttu-id="1b153-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b153-125">RELATED LINKS</span></span>
